# Common Problems

### HTTPS issue

By default, **Jet Bridge** will run in **HTTP** mode while **Jet Admin** opens in **HTTPS**. This can lead to a similar error when trying to connect to Jet Bridge running under HTTP:

> Mixed Content: The page at 'https://app.jetadmin.io/builder/...' was loaded over HTTPS, but requested an insecure XMLHttpRequest endpoint 'http://JET\_BRIDGE\_HOST/api/discover/connection/'. This request has been blocked; the content must be served over HTTPS.

You have several options how to fix this issue:

1. Run **Jet Bridge** in **HTTPS** mode using `SSL_CERT` and `SSL_KEY` options (see [Configuration](configuration.md)). You will need an SSL **certificate** and **private key** for the domain name under which **Jet Bridge** is running. If you don't have an **SSL certificate** you can create self-signed **SSL certificate** files `.crt` and `.key` ([Manual](https://www.digitalocean.com/community/tutorials/how-to-create-a-self-signed-ssl-certificate-for-nginx-in-ubuntu-22-04)).
2. Run **Jet Bridge** behind a web server with **HTTPS** configured (for example **nginx**).
3. (_for Test purposes_) You can use **Jet Admin** in **HTTP** mode. We allow you to open your App in **HTTP** mode if you change **HTTPS** to **HTTP** in your browser URL. Be sure to connect to **Jet Bridge** with http:// on your browser URL otherwise, you will get a connection error.

{% hint style="info" %}
For testing, you can use [Ngrok](https://ngrok.com/docs/getting-started/) service to put your application on the internet via HTTPS
{% endhint %}

### CORS issue

If you are deploying **Jet Bridge** behind a proxy or some webserver you can start receiving the following errors in your browser console:

> Access to XMLHttpRequest at '...' from origin 'https://app.jetad.io.io' has been blocked by CORS policy: Response to preflight request doesn't pass access control check: No 'Access-Control-Allow-Origin' header is present on the requested resource.

Normally you shouldn't have this issue as **Jet Bridge** automatically adds the appropriate **CORS** headers to all responses.

#### Behind Nginx

To fix the **CORS** issue for **Nginx** add the following to jetbridge.yourdomain.com.conf:

{% code title="my-website.conf" %}
```
server {
    listen 80;

    server_name jetbridge.yourdomain.com;

    return 301 https://$host$request_uri;
}

 server {
      listen 443 http2 ssl;
      ssl_certificate /etc/nginx/ssl/yourdomain.com.crt;
      ssl_certificate_key /etc/nginx/ssl/yourdomain.com.key;
      server_name jetbridge.yourdomain.com; 

    location / {
      ###################################
      # START
      # Add this block to your location
      ###################################
      
      proxy_hide_header 'Access-Control-Allow-Origin';
      proxy_hide_header 'Access-Control-Allow-Methods';
      proxy_hide_header 'Access-Control-Allow-Headers';
      proxy_hide_header 'Access-Control-Expose-Headers';

      if ($request_method = 'OPTIONS') {
        add_header 'Access-Control-Allow-Origin' '*' always;
        add_header 'Access-Control-Allow-Methods' 'GET, POST, PUT, PATCH, DELETE, OPTIONS';
        add_header 'Access-Control-Allow-Headers' 'Authorization,DNT,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Range';
        add_header 'Access-Control-Max-Age' 1728000;
        add_header 'Content-Type' 'text/plain; charset=utf-8';
        add_header 'Content-Length' 0;
        return 204;
      }

      add_header 'Access-Control-Allow-Origin' '*' always;
      add_header 'Access-Control-Allow-Methods' 'GET, POST, PUT, PATCH, DELETE, OPTIONS';
      add_header 'Access-Control-Allow-Headers' 'Authorization,DNT,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Range';
      add_header 'Access-Control-Expose-Headers' 'Content-Length,Content-Range';
      
      ###################################
      # END
      ###################################
      
      proxy_pass http://127.0.0.1:8888; # default port for jet-bridge
    }
}
```
{% endcode %}

{% hint style="info" %}
If you don't have a certificate for https you can use Let’s Encrypt.  A free and open Certificate Authority (CA), provides an easy and automated way to obtain SSL certificates. &#x20;
{% endhint %}

**To install Certbot, follow these steps:**

<pre class="language-bash"><code class="lang-bash">#For Ubuntu/Debian:
sudo apt-get update
sudo apt-get install certbot

#For CentOS/RHEL:
sudo yum install certbot

#To obtain a Let’s Encrypt SSL certificate for your domain, run the following Certbot command:
sudo certbot certonly --nginx -d yourdomain.com

<strong>#If successful, the certificate and private key will be stored in /etc/letsencrypt/live/yourdomain.com/
</strong><strong>
</strong>#make the following changes in jetbridge.yourdomain.com.conf:
    ---
      ssl_certificate /etc/nginx/ssl/yourdomain.com.crt; -> ssl_certificate /etc/letsencrypt/live/yourdomain.com/fullchain.pem;
      ssl_certificate_key /etc/nginx/ssl/yourdomain.com.key; -> ssl_certificate_key; /etc/letsencrypt/live/yourdomain.com/privkey.pem;
    ---
    
#Let’s Encrypt certificates have a validity of 90 days. To ensure uninterrupted SSL protection, automating the certificate renewal process is essential. Certbot provides a renew command that you can schedule to run periodically.
<strong>
</strong><strong>#To add a renewal cron job, open the crontab editor:
</strong><strong>sudo crontab -e
</strong>
#Add the following line to run the renewal check daily:
0 0 * * * certbot renew --nginx --quiet
</code></pre>

This is because newer versions of the **Pillow** Python library are incompatible with **Python 3.4 or lower**. Install an older version to fix this error:

```python
pip install pillow==4.3.0
```

### \[Python 3.4 or lower] Error when running Jet Bridge: AttributeError: 'module' object has no attribute 'module\_from\_spec'

This is because newer versions of the **date parser** Python library are incompatible with **Python 3.4 or lower**. Install an older version to fix this error:

```python
pip install dateparser==0.7.1
```

### \[Django] Fields generated by django-modeltranslation package does not displaying and saving correctly

The problem is that `django-modeltranslation` patches **Django** models so you need to load `jet_django` package only after `django-modeltranslation` has finished its patching this way in your `settings.py`:

```python
INSTALLED_APPS = (
    ...
    'modeltranslation',
    'jet_django', # load after modeltranslation
    ...
)
```

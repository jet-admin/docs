# Deploy On-Premise Jet Admin with Docker

This deployment method grants you access to the full suite of Jet Admin services, empowering your workflow with comprehensive functionality.

### **Install On-Premise Jet Admin:**

Navigate to the environment settings. From the left menu, select "On-premise" and designate the app deployment type as "On-premise".

{% @arcade/embed flowId="Ims6qU1aaFAnsQR1t8sa" url="https://app.arcade.software/share/Ims6qU1aaFAnsQR1t8sa" %}

*   Open a terminal or command prompt and execute the following command:

    ```less
    sudo sh -c "$(curl -sS https://link-dev.jetadmin.io/install/o23b1j05tktey5glysf504xm6ayi5mklao3kuf60ltt9jzjl)"
    ```
* This command retrieves a script from the specified URL (https://link-dev.jetadmin.io/install/o23b1j05tktey5glysf504xm6ayi5mklao3kuf60ltt9jzjl) and runs it using `sh`.&#x20;
* This script will handle the installation process for the Jet Admin package

{% @arcade/embed flowId="sy4XxY3gw8I29VvURo3v" url="https://app.arcade.software/share/sy4XxY3gw8I29VvURo3v" %}

### **Run Jet Admin On-Premise:**

* After the installation is complete, you can run Jet Admin on-premise using Docker-compose.
* Navigate to the jet-onpremise directory where Jet Admin is installed.
*   Run the following command to start Jet Admin and its components in the background:

    ```
    sudo docker-compose up -d
    ```

{% @arcade/embed flowId="OopbagL25zQ2aLu1SUyO" url="https://app.arcade.software/share/OopbagL25zQ2aLu1SUyO" %}

* The application should now be accessible at the specified NGINX port (default is 80) on your localhost (`http://localhost:80`).

1. **Verification:**
   * To verify that Jet Admin is running, open a web browser and navigate to `http://localhost:80`.
   * Proceed to create a new account, then create a project and add resources.

{% @arcade/embed flowId="ssc8tWflHfNwg2G9XjXy" url="https://app.arcade.software/share/ssc8tWflHfNwg2G9XjXy" %}

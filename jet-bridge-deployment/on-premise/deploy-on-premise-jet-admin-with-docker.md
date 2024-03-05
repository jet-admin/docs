---
description: Learn how to deploy an instance of On-Premise Jet Admin using Docker-compose.
---

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

{% embed url="https://www.loom.com/share/688fec3577de4681b4c769f1354dfa68?sid=e368e4ea-37e9-4693-8127-ddb723dfefdf" %}

### **Run Jet Admin On-Premise:**

* After the installation is complete, you can run Jet Admin on-premise using Docker-compose.
* Navigate to the jet-onpremise directory where Jet Admin is installed.
*   Run the following command to start Jet Admin and its components in the background:

    ```
    sudo docker-compose up -d
    ```
* The application should now be accessible at the specified NGINX port (default is 80) on your localhost (`http://localhost:80`).

{% embed url="https://www.loom.com/share/a55213e22f854f8ca086932cc5cbe876?sid=8bcf4961-de80-4da3-96a0-e0a414234675" %}

### **Verification:**

* To verify that Jet Admin is running, open a web browser and navigate to `http://localhost:80`.
* Proceed to create a new account, then create a project and add resources.

{% embed url="https://www.loom.com/share/04a605f83cda438d9d63f72e59c7375c?sid=95cd8a8f-82bc-46e3-b27f-fa9d6de5125f" %}

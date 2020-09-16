
# Essential Cloud Infrastructure: Foundation
These courses introduce you to the comprehensive and flexible infrastructure and platform services provided by Google Cloud Platform (GCP), with a focus on Compute Engine:
1. Essential Cloud Infrastructure: Foundation (this course)

2. Essential Cloud Infrastructure: Core Services

3. Elastic Cloud Infrastructure: Scaling and Automation

**LAB 1: Getting started with cloud marketplace**

-step 1: (Google Cloud console)[https://console.cloud.google.com]

-step 2 : login with your account

-step 3 : Create project in your cloud console dashboard

-step 4 : launch the cloud shell or Open a terminal window

In this lab, you use Cloud Marketplace to quickly and easily deploy a LAMP stack on a Compute Engine instance. The Bitnami LAMP Stack provides a complete web development environment for Linux that can be launched in one click.

For more information on the Bitnami LAMP stack, see (Bitnami LAMP Stack Documentation)[https://docs.bitnami.com/google/infrastructure/lamp/].

## Use Cloud Marketplace to deploy a LAMP stack

1.In the GCP Console, on the Navigation menu (), click Marketplace.

2.In the search bar, type LAMP

3.In the search results, click LAMP Certified by Bitnami.
If you choose another LAMP stack, such as the Google Click to Deploy offering, the lab instructions will not work as expected.

4.On the LAMP page, click Launch.
If this is your first time using Compute Engine, the Compute Engine API must be initialized before you can continue.

5.For Zone, select the deployment zone that Qwiklabs assigned to you.

6.Leave the remaining settings as their defaults.

7.If you are prompted to accept the GCP Marketplace Terms of Service, do so.

8.Click Deploy.

9.If a Welcome to Deployment Manager message appears, click Close to dismiss it.
The status of the deployment appears in the console window: lampstack-1 is being deployed. When the deployment of the infrastructure is complete, the status changes to lampstack-1 has been deployed.
After the software is installed, a summary of the details for the instance, including the site address, is displayed.

### Verify your deployment
1.When the deployment is complete, click the Site address link in the right pane.
Alternatively, you can click Visit the site in the Get started with LAMP Certified by Bitnami section of the page. A new browser tab displays a congratulations message. This page confirms that, as part of the LAMP stack, the Apache HTTP Server is running.

2.Close the congratulations browser tab.

3.On the GCP Console, under Get started with LAMP Certified by Bitnami, click SSH.

4.In a new window, a secure login shell session on your virtual machine appears.
In the just-created SSH window, to change the current working directory to /opt/bitnami, execute the following command:
`cd /opt/bitnami`

5.To copy the phpinfo.php script from the installation directory to a publicly accessible location under the web server document root, execute the following command:
`sudo sh -c 'echo "<?php phpinfo(); ?>" > apache2/htdocs/phpinfo.php'`

6.The phpinfo.php script displays your PHP configuration. It is often used to verify a new PHP installation.

7.To close the SSH window, execute the following command:
`exit`

8.Open a new browser tab.

9.Type the following URL, and replace SITE_ADDRESS with the URL in the Site address field in the right pane of the lampstack page.

(lampstack)[http://SITE_ADDRESS/phpinfo.php]

The URL from the lab was as follows;

(lampstack)[http://35.226.195.168/phpinfo.php]

10.A summary of the PHP configuration of your server is displayed.

11.Close the phpinfo tab.






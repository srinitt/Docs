.. meta::
   :description: Create GCloud Account on Aviatrix Controller
   :keywords: GCloud, create GCloud, create GCloud account, Aviatrix, GCP credentials




===================================================================
GCP Credentials
===================================================================


Before creating a cloud account for GCloud/GCP on Aviatrix controller, go through the
steps below to make sure you have the credentials setup for API calls.


Step 1: Create a GCloud Account
-------------------------------

Create a GCloud or GCP account (https://cloud.google.com/). Go on to the next
step if you have already done so.

Note that the controller supports multiple accounts with each one
associated with a different GCloud projects, but there needs to be at
least one to start with.

Step 2: Create a GCloud Project
---------------------------------

Login to your GCloud account and go to project page:
https://console.cloud.google.com/project

Create a project. Go on to the next step if you have already created
one. Note the project ID will be used in referencing to the project by
Aviatrix controller.

(As an example, we created a project Aviatrix-UCC, the project ID is
aviatrix-ucc-1214)

Step 3: Enable Compute Engine API
----------------------------------

Enable Compute Engine API on the selected project,

1. go to your Google Cloud Platform console, at the upper left corner
   left to Google Cloud Platform signage, click the 3 bars. A drop down
   menu will appear.

2. Select API Manager, at Google Cloud APIs, select Compute Engine API.

3. click Enable.

Step 4: Enable GCloud Messaging Service
-------------------------------------------

Aviatrix controller uses GCloud Pub/Sub messaging service to communicate
with the gateways.

To enable Pub/Sub on the selected project,

1. go to your Google Cloud Platform console, at the upper left corner
   left to Google Cloud Platform signage, click the 3 bars. A drop down
   menu will appear.

2. Select API Manager, at Google Cloud APIs, click more to expand.

select Cloud Pub/Sub API, as shown below, then click Enable.

|image0|

Step 5: Create Credential File
----------------------------------

When you create a cloud account for GCloud, you are asked to upload a
GCloud Project Credentials file. Below are the steps to download the
credential file from Google Developer Console.

1. Open the `Credential
   page <http://console.developers.google.com/project/_/apiui/credential>`__

2. Select the project you are creating credentials for.

3. At Credentials, Click Create credentials, select Service account key,
   as shown below

   |image1|

4. At the Service account dropdown menu, select Compute Engine default
   service account, select JSON.

5. Click Create. The credential file will be downloaded to your local
   computer.

6. Upload the Project Credential file to Aviatrix controller at GCloud
   account create page.

Troubleshooting Tips
----------------------

If cloud account creation fails, check the error message at the Aviatrix
controller console and try again with the steps provided in this
document.

For additional support, send email to support@aviatrix.com

.. |image0| image:: GCloud_media/image1.png

.. |image1| image:: GCloud_media/image2.png

.. disqus::

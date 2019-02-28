# Create your first Wix Application on your machine Tutorial  
In this tutorial we go over how to create a Wix Application that interacts with the Wix platform 
and you will be hopefully can submit it for the Wix Application Market, So Wix site owners can deploy it on their sites.   
## 1. Creating an Application on Wix Developers
First we need to go to [Wix Developers](https://dev.wix.com/) and login/signup to Wix Developers.
Than create a new application by clicking 

![Create New App](images/create-app.png)

You should get this screen:

![Create New App](images/New-App.png)

Go to Workspace/OAuth and copy your `App ID` and `App Secret ID`. You will need them later.
 
![Create New App](images/oauth-settings.png)

## 2. Getting your app and run it

Download and install [npm](https://www.npmjs.com/get-npm)

Clone the [Wix Sample Application](https://github.com/shaykewix/sample-wix-rest-app)

Edit index.js and replace the APP_ID and APP_SECERT with the values from the Wix Developer site:
![Create New App](images/change-app-id.png)

### Run your application
run `npm install`

run `npm build`

run `npm build`

You should get:

![Listening](images/listening.png)

## 3. Setup the application for receiving inbound HTTPS connections
Since most developers machine are not open for inbound connection and don't has HTTPS certificates, we will use **ngrok**.
If you are hosting your application on a server without those restriction, you can skip this step.

### Install and run [ngrok](https://dashboard.ngrok.com/get-started)

You should get something like:

![ngrok screen](images/ngrok.png)

**Dont't close the ngrok process** - You will need for the entire process.

### Setup your application URLs
Go to Workspace/OAuth and fill the **`Redirect URL`** `with https://12345678.ngrok.io/login`

Go to Workspace/OAuth and fill the **`App URL`** `with https://12345678.ngrok.io/signup`

**Remeber to replace '12345678' with ** your ngrok string yout got in your screen.**
for example:

![Listening](images/httpsurl.png)

 
![update application urls](images/urls.png)

Don't forget to click the Save button on the bottom right 

![save](images/save.png)

## Your application should be now ready for installation and first output! 

1. Click the `Test Your App` on the top right:
![test your app](images/test-button.png)

2. Click `Test Your App`:

![site selector](images/site-selector.png)

3. Click `Add To Site`:

![site selector](images/add-to-site.png)

4. Approve the consent page by clicking `Allow and Install`:

![site selector](images/consent.png)

5. You should get a print into the browser with your application ID and your site instance ID:
![site selector](images/end.png)

# You are done!
## You can now add your Application logic and Other WIX APIs. 

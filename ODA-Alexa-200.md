Updated: October 14th, 2019

## Introduction

In this lab we will explain how to setup a heroku server leveraging the existing NodeJS server found [here](https://blogs.oracle.com/mobile/adding-alexa-as-a-conversation-channel-to-your-oracle-digital-assistant-chatbot)
You will use various commands to install heroku on your local environment. 

## Objectives
- Create Heroku Account
- Setup Heroku on local computer
- Prepare the application
- Deploy the application
- Configure NodeJS server
    - Update Amazon AppID
    - Update Channel Secret Key and Channel URL 
- Redeploy NodeJS server on Heroku
    - Setup (Install heroku on your local environment
    - Prepare the application
    - Deploy the application
    - View the logs

## Required Artifacts
- Oracle Digital Assistant Skill
- Heroku Account
- Download the NodeJS code [here](https://blogs.oracle.com/mobile/adding-alexa-as-a-conversation-channel-to-your-oracle-digital-assistant-chatbot)

# Create Heroku Account
Follow this [link](https://signup.heroku.com/?c=70130000001xDpdAAE&gclid=Cj0KCQjwuZDtBRDvARIsAPXFx3DyRB323ksXfO_lYs7W14RB6CRCTQjMBNQTOuElUazr4rbuGysu78waAvLDEALw_wcB) to create a heroku account. 

# Heroku setup
Follow this [link](https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up) to set up Heroku on a local computer

# Change package.json
Inside of the nodejs server you downloaded there is a file called package.json. Copy and replace with the code below. 
```
{
  "name": "oracle-bot-alexa",
  "version": "1.0.0",
  "description": "Alexa integration",
  "main": "service.js",
  "author": "",
  "license": "",
  "dependencies": {
    "@oracle/bots-node-sdk": "2.0.6",
    "alexa-app": "^4.2.0",
    "body-parser": "^1.15.2",
    "express": "^4.14.0",
    "pubsub-js": "^1.5.4",
    "underscore": "^1.8.3",
    "util": "^0.10.3"
  },
  "scripts": {
    "start": "node index.js"
  }
} 
```
# Heroku application deployment
## Follow the below steps to create an app in heroku and deploy the sample code
### **STEP 1**: Go to heroku dashboard and create an app
  Give it any name you want.
  ***OR***
  Create an app from the [cli](https://devcenter.heroku.com/articles/creating-apps)

### **STEP 2**: Open NodeJS directory
  - In your terminal go **INTO** the nodejs directory you downloaded.
  - Run the following commands in terminal: 
  
    **Create a new GIT repo**
    ```
    heroku login
    git init
    heroku git: remote -a <INSERT APP NAME>
    ```

    **Deploy your application**
    ```
    git add .
    git commit -am "some comment"
    git push heroku master
    ```

# Create webhook in Oracle Digital Assistant
  ## In this section we will create a webhook in Oracle Digital Assistant, change service.js, and redeploy the application.
  ### **STEP 1**: Go to your Oracle Digital Assistant Instance.
  ### **STEP 2**: Create a channel of type "Webhook".
    Give it a name of your choice. For the "Outgoing webhook URI", go to your heroku app, **click open app**, and copy that    link. The **outgoing webhook URL** will be: **/<URL-THAT-YOU-JUST-COPIED/>/singleBotWebhook/messages** 
  ### **STEP 3**: Copy SECRET KEY.
  ### **STEP 3**: Copy Webhook URL.
   

  
# Redeploy nodejs application
## Before we redeploy the NodeJS application we need to make some changes in ***service.js***
### **STEP 1**: Open service.js in a code editor
### **STEP 2**: Change amazon application ID in service.js

- **Use the amazon application id you copied earlier and copy it here** :
![](images/200heroku/appID.png)
  


**This completes the ODA-Alexa Integration Workshop!**


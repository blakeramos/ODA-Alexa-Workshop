# ODA-Alexa Integration - Alexa Set Up

This part of the lab builds the Alexa side of the integration.

## Objectives

- Creating a Skill
- Configuring the Skill

## Steps

### **STEP 1**: Your Amazon Developer Account

- If you do not have a developer account, sign up for one here: [Sign Up](https://developer.amazon.com/en-US/alexa/alexa-skills-kit/start)

### **STEP 2**: Log in to your account

- Sign in to the developer console using your Amazon Developer account. This may require a one-time PIN which will be sent to your email. 

### **STEP 3**: Creating a Skill

- Ensure Skills Tab is selected 

- Click **Create Skill**.

  ![](images/100ODA/alexa-create-skill-1.png)

- Enter your skill name. Under **Choose a model to add**, select 'Custom'. Under **Choose a method to host your skill's backend resources**, select 'Provision your own'. 

  ![](images/100ODA/alexa-create-skill-2.png)

  ![](images/100ODA/alexa-create-skill-3.png)

- Click **Create Skill**.

- From **Choose a template**, select 'Start from scratch'.

  ![](images/100ODA/alexa-create-skill-4.png)

### **STEP 4**: Define the Skill

- From the created skill, select the **Invocation** option on the left panel.

<img src="images/100ODA/alexa-setup-skill-1.png" width="200px">

- Under **Skill Invocation Name**, enter the phrase you would like to invoke the bot (must be 2 words).

  ![](images/100ODA/alexa-setup-skill-2.png)

- Select the **Slot Types** option on the left panel. 

  ![](images/100ODA/alexa-setup-skill-3.png)

- Select **Add Slot Type**. Select **Create custom slot type** and enter a name for your slot. 

  ![](images/100ODA/alexa-setup-skill-4.png)

  ![](images/100ODA/alexa-setup-skill-5.png)

- Enter a name for your slot into the **Slot Values** textbox. 

  ![](images/100ODA/alexa-setup-skill-6.png)

- Find the **Intent** option on the left panel.

  ![](images/100ODA/alexa-setup-skill-7.png)

- Create a new Intent with the **Add Intent** button

  ![](images/100ODA/alexa-setup-skill-8.png)

- Select **Create custom intent** and enter a name for your intent. This name cannot be the same as your slot name that you created previously. 

  ![](images/100ODA/alexa-setup-skill-9.png)

- In **Sample Utterances**, enter {command}

  ![](images/100ODA/alexa-setup-skill-10.png)

- Scroll down and find **Intent Slots**. For 'command' select your custom slot type as the slot type. 

  ![](images/100ODA/alexa-setup-skill-11.png)

### **STEP 5**: Note the Skill ID

- Scroll to the top of the page and press the 'Your Skills' option. 

  ![](images/100ODA/alexa-setup-skill-12.png)

- Find your skill in the list, and click 'View Skill ID'. Write down this ID, as we will be using it later. 

  ![](images/100ODA/alexa-setup-skill-13.png)

**This completes the Set Up!**

**You are ready to proceed to [Lab 200](ODA-Alexa-200.md)**


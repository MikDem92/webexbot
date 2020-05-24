# Webex Teams Bot - Template

Cisco's Webex Teams offers a woderful platform for bot creation. However, 
many people who are new to the world of ChatOps and Cisco's REST APIs are
struggling with creation of bots and their integration with existing services.
So, the goal of this project is to provide a simple to use template for
creating and setting up Webex Teams bots. It provides a ready-to-use framework
for bot development with the back-and-forth communication between the Webex
Teams client, the Webex cloud and the bot server already been implemented.
The only thing that the users need to do by themselves is creating the actual
bot functionality. 

The template is written in PHP, because it is the most common language for
backend development. The webhook creation and registration script is written 
in Python as it is a simple solution for creating a script that can be run
right away. This being said, the bot itself can be written in any language 
and then be executed with the **exec()** from inside PHP. Therefore, this
template can serve as a wrapper for the bot functions written in the users'
language(s) of choice.

---
## Table of Contents
  * [1. Requirements](#1-requirements)
  * [2. Setup](#2-setup)
    + [Edit setup file](#edit-setup-file)
    + [Register webhook](#register-webhook)
    + [Create bot logic](#create-bot-logic)
 * [Authors and Maintainers](#authors-and-maintainers)
 * [Disclaimer](#disclaimer)

---

## 1. Requirements

In order to run the bot in operation, you need the following:
- A web-server running PHP7
- Reachability to the Webex cloud
- Python 3.X with **requests** and **json** libraries installed
- Webex Teams bot credentials (*access token* and *bot ID*) from developer.webex.com

---

## 2. Setup

After copying the repository to your server, the bot need to be set up for development, testing and operation.
This is done in three steps that need to be completed in the following order:
- Edit **setup.json**
- Register the webhook with **register.py**
- Edit **webexbot.php** to add some functionality to the bot

### Edit setup file
The **setup.json** file serves as a container for all the environment variables needed to set up the bot.
By default, all the variables are blank, so you need to fill in your personal information:
- **target_url:** The URL of the folder inside your server where all the bot files are hosted
- **webhook_name:** An arbitrary name for the webhook
- **access_token:** Access token of the bot
- **bot_id:** Bot ID

### Register webhook
As a next step you need to create and register a webhook. For this, open up the console inside the repository folder
and type in:

**python3 register.py**

### Create bot logic
Now, in order to create some functionality for the bot, you need to edit **webexbot.py** inside the */includes*
folder. Go to the *answer()* function and edit the highlighted part of the code at your will.

---

## Authors and Maintainers

I am the sole author and maintainer of the project. If you have any questions, comments and/or suggestions,
do not hesitate to contact me directly.

---

## Disclaimer

This project is in no way related to my current or past employers. It is a product of my own and is created and maintained
merely as a display of my personal work. It is available for free and fair use. However, I do not hold any responsibility
for any damage it may cause when deployed in a production environment.

### Webex Teams Bot - Template

Cisco's Webex Teams offers a woderful platform for bot creation. However, 
many people who are new to the world of ChatOps and Cisco's REST APIs are
struggling with creation of bots and their integration with existing services.
So, the goal of this project is to provide a simple to use template for
creating and setting up Webex Teams bots. It provides a ready-to-use framework
for bot development with the back-and-forth communication between the Webex
Teams client, the Webex cloud and the bot server already been implemented.
The only thing that the users need to do by themselves is creating the actual
bot logic. 

The template is written in PHP, because it is the most common language for
backend development. The webhook creation and registration script is written 
in Python as it is a simple solution for creating a script that can be run
right away. This being said, the bot itself can be written in any language 
and then be executed with the exec() from inside PHP. Therefore, this
template can serve as a wrapper for the bot functions written in the users'
language(s) of choice.

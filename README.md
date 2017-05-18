# botframework-skype-calling-example-bot
Example Skype Calling Bot for Bot Framework Node SDK

#### For more information on Skype Calling support in Bot Framework see:
https://docs.microsoft.com/en-us/bot-framework/nodejs/bot-builder-nodejs-conduct-audio-calls

#### botbuilder-calling on NPM:
https://www.npmjs.com/package/botbuilder-calling


#### Overview
This Bot is a sample calling bot for Skype.  It's designed to showcase whats 
possible on Skype using the BotBuilder SDK. The demo shows how to create a 
looping menu, recognize speech & DTMF, record messages, play multiple prompts,
and even send a caller a chat message.

#### Run the bot:

You can run the bot locally using ngrok found at [https://ngrok.com/](https://ngrok.com/)

- Install and run ngrok in a console window using "ngrok http 3978".
- Create a bot on [https://dev.botframework.com](https://dev.botframework.com) and follow the steps to setup
    a Skype channel. Ensure that you enable calling support for your bots skype
    channel. 
- For the messaging endpoint in the Details for your Bot at dev.botframework.com,
    ensure you enter the https link from ngrok setup and set
    `<ngrok link>/api/messages` as your bots calling endpoint.
- For the calling endpoint you setup on dev.botframework.com, copy the https 
    link from ngrok setup and set `<ngrok link>/api/calls` as your bots calling 
    endpoint.
- Next you need to configure your bots `CALLBACK_URL`, `MICROSOFT_APP_ID`, and
    `MICROSOFT_APP_PASSWORD` environment variables. If you're running VSCode you 
    can add these variables to your the bots launch.json file. If you're not 
    using VSCode you'll need to setup these variables in a console window.
    - `CALLBACK_URL`: This should be the same endpoint you set as your calling
            endpoint in the developer portal.
    - `MICROSOFT_APP_ID`: This is the App ID assigned when you created your bot.
    - `MICROSOFT_APP_PASSWORD`: This was also assigned when you created your bot.
- To use the bot you'll need to click the join link in the portal which will
    add it as a contact to your skype account. When you click on the bot in 
    your skype client you should see an option to call your bot. If you're 
    adding calling to an existing bot can take up to 24 hours for the calling 
    option to show up.
- You can run the bot by launching it from VSCode or running "node app.js"
    from a console window.  Then call your bot from a skype client to start
    the demo. 

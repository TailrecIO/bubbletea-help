# How to Fix "The bot cannot access the private channel."

A bot in Slack operates similarly to a user. If you are not a member of a private channel, you cannot view 
or post messages there. Therefore, if you receive an error message such as 'the bot cannot access the private channel',
it implies that you need to invite the bot to the private channel.

![fix-bot-access-1.png](images%2Ffix-bot-access-1.png)

The access error message typically prompts you to invite the Bubble Tea bot to your private channel and provides 
an example in the code block. Be careful not to directly copy and paste `/invite @Bubble Tea` because Slack may retain 
the formatting, causing the formatted message to not trigger the `/invite` command. So, the safest option is to type it manually.


![fix-bot-access-2.png](images%2Ffix-bot-access-2.png)

After successfully executing the invite command, you should see a message similar to the one in the screenshot above. 
Once Bubble Tea is added to your channel, you can make use of its powerful features there.

If it's still not working for you, please send us an email at support@bubbletea.cloud, and we will get back to you as soon as possible
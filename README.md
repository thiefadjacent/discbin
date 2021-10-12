# discbin
Bash utility for sending any command's output to a discord webhook.

## usage

For example, the command...
>`cat example.txt | discbin https://discord.com/api/webhooks/example`

will read a file and send its contents to the webhook at the above URL.
\
\
Once a webhook URL has been used, discbin will remember it until a new one is supplied. Thus...
>`cat another_example.txt | discbin`

will send to the URL specified earlier.
\
\
*N.B.: discbin, consequentially, is self-modifying, and any user who runs discbin must also have permission to edit the discbin file.*

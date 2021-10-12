# discbin
Bash utility for sending any command's output to a discord webhook 


For example, the command
`cat example.txt | discbin https://discord.com/api/webhooks/example`
will read the contents of `example.txt` and send them to the webhook at the above URL.

Once the webhook has been added, discbin will remember that URL until a new one is supplied. Thus,
`cat another_example.txt | discbin`
will send to the URL specified earlier.


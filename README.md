# discbin
Bash utility for sending any shell command's output to a discord webhook.

## Basic Usage

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
*NB: discbin, consequentially, is self-modifying, and any user who runs discbin must also have permission to edit the discbin file.*


## Continuous Logging

Discbin can be used with `watch` in order to continuously send information to a webhook. For example...
>`watch -n 60 "tail /var/log/syslog | discbin"`

will send the last 10 lines of the syslog to your webhook once every 60 seconds.

You could also run discbin + watch as a background job:
>`watch -n 60 "tail /var/log/syslog | discbin" &>/dev/null &`

remember that you can reattach to the job with `fg`. 

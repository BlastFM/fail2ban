# Fail2ban Modified Recidive Jail
## Working in Ubuntu but might need some small modification for other systems
`Settings for fail2ban persistent ofenders using the built in recidive filters and a modified log rotation for fail2ban`

>Some modifications need to be made to make the recidive jail work properly. The fail2ban log rotation default needs to be changed because we don't want it to compress the logs daily, we want one log file which will hold 4 weeks of data.

`The fail2ban file contains the modified log rotation schedule`

>The only change here from the default is to change the dailycompress option to compress.

`The file jail.local containes the modified local jail which includes ssh, ssh-ddos, postfix-sasl, recidive in this case. Adjust to suit your needs.`

>It also has a modified logpath to wildcard match all fail2ban* files in the log directory, for fail2ban.log.1, fail2ban.log.2 etc so that it does not stop reading the log files when they rotate.

You can contact us at https://blastfmsocial.media or https://blastfm.limited

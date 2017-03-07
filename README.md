# complete sites backups
#erev0s

This script is made in an effort to automate the procedure of backing up sites.
You can use your pushover account with it and your email account to receive notifications that the backup went well
I have included a check on mysqldump so you would know if the process ended with an error.


    it creates the path to store the databases
    it deletes files in this path that are older than 5 days
    it echoes all databases
    it skips schema databases and all databases with underscore
    it backups up databases and notifies if any database dump ends with error
    it emails the results to you, and send them through pushover too



You can add this shell script to a cronjob to run every a couple of days

in order to do this you need to run

crontab -e

and add there your script according to your needs

0 0 */2 * * /root/tools/dbbackup.sh 2>/dev/null



###########-to do list-###########

############################
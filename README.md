# Crontab-curl
Execution du cron qui accède à google.com via curl et fait la jornalisation

# créé deux fichier
touch /home/kali/curl/script2.sh
touch /home/kali/curl/scriptLog.log

# acceder dans le fichier et mettre les instructions
vim /home/kali/curl/script2.sh 

#!/bin/bash
curl https://www.google.com 

# creation cron avec execution et journalisation dans scriptLog.log
crontab -e

*/1 * * * * * /home/kali/curl/script2.sh >> /home/kali/curl/scriptLog.log




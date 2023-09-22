# digitalocean_attacker_scripts
This repo contains an actual attack performed on my Digital Ocean droplet serving a couple of websites.

## Some info as to what is what:
1. .configrc5 is a folder which contains scripts that are executed by a crontab.
2. .ssh contains authorized keys. the attacker used keys to gain access to the account name **madhu**.
3. dev/shm/.Xzqo has some files regarding rsync which probably the attackers use to sync the scripts
4. /etc/ is just a copy of my system's /etc/ folder since this was changed too.
5. auth.log is from the machine too
6. crontab_mod.txt is what I found in the crontab, which executed the scripts in .configrc5 regularly
7. syslog is from the machine again
8. terminal_ss_1.png is just a ss containing output of terminal when i typed the commands ``` sudo grep -i "Accepted" /var/log/auth.log ``` and ``` sudo grep -t "madhu" /var/log/auth.log ```
9. abuse_report_digital_ocean.pdf is the abuse report which prompted the incident. 

## Would appreciate your help if you can decode what the scripts are doing. 
As far as i know, they used my machine to attack more machince and use ssh brute force attacks.


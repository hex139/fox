Check my notion template 

https://codine7.notion.site/FOX-Scanner-21cc291a4b474bfe87df81557c57e87d?pvs=4


```
uncover -e shodan,shodan-idb,fofa,censys,quake,hunter,zoomeye,netlas,publicwww,criminalip,hunterhow -q $1 -o uncoverOutput.fox
```

```
nuclei -c 200 -bs 50 -tags database,mongo,mysql,firebase,redis,stripe,paypal,bitcoin,odoo,rails,aws,azure,env -es info,low,medium -l $1 -o nucleiOutput.fox | notify -pc discord.yaml
```

# Cron Job
```
*/10 * * * * ~/dragon/fly.sh > ~/dragon_cron_log.txt 2>&1
```



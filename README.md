# Cisco Spark Widgets Samples

If you're new to Widgets, we recommend you take the [Space Widget demo](https://code.s4d.io/widget-space/latest/demo/index.html)


[Spark Widgets](https://developer.ciscospark.com/widgets.html) are opensource React components that let you integrate Cisco Spark Messaging & Audio/Video into your web apps 

**Place your Cisco Spark access tokens before opening each widget sample (sometimes a roomId is required too)**


## Tip to dynamically inject tokens and parameters

Using [Caddy template actions](https://caddyserver.com/docs/template-actions), it's possible to customize the samples by injecting your own token (with the SPARK_TOKEN env variable) and query parameters on the URL (?roomId=, ?sip= , ?email= ). Read instructions below.

Download caddy: https://caddyserver.com/download

Run the commands below from bash shell, and access the samples at ':9000/'

```bash
git clone <repo>
cd repo
SPARK_TOKEN=access_token  caddy 
```

Examples:
   - http://localhost:9000/
   - http://localhost:9000/recents/widget-recents-global.html
   - http://localhost:9000/together/both-recents-and-space.html

   - https://localhost:9443/space/widget-space-data-meet-sip.html
   - https://localhost:9443/space/widget-space-data-meet-sip.html?sip=roomkit@sparkdemos.com

   - http://localhost:9000/space/widget-space-data-spaceid.html?roomId=Y2lzY29zcGFyazovL3VzL1JPT00vNWU5YzM3YTAtMDFkOC0xMWU4LTg1NDgtMDFiYmYxOTZlZDNm

   - http://localhost:9000/space/widget-space-data.html?email=CiscoDevNet@sparkbot.io
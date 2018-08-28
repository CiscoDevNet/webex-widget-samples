# Cisco Webex Teams Widgets Samples

[Webex Teams Widgets](https://developer.webex.com/widgets.html) are open-source React components that let you integrate Cisco Webex Teams Messaging & Audio/Video into your web apps.

If you're new to Widgets, we recommend you try the [Space Widget demo](https://code.s4d.io/widget-space/latest/demo/index.html).

**Enter the 'static' directory, and update each example with a Cisco Webex Teams API access token (sometimes a `roomId` is required too).**

## Tip to dynamically inject Cisco Webex Teams access tokens

Using [Caddy template actions](https://caddyserver.com/docs/template-actions), it's possible to customize the samples by injecting your own token (with the `ACCESS_TOKEN` env variable) and query parameters on the URL (`?roomId=`, `?sip=`, `?email=`). Read instructions below.

Download caddy: https://caddyserver.com/download, and add the command to your path.

Run the commands below from bash shell, and access the samples at ':9000/'

```bash
git clone https://github.com/CiscoDevNet/widget-samples
cd widget-samples
cd caddy
# Starts caddy with a Cisco Webex Teams API access token (check https://developer.webex.com)
ACCESS_TOKEN=access_token  caddy
```

Examples:

- http://localhost:9000/
- http://localhost:9000/recents/widget-recents-global.html
- http://localhost:9000/together/both-recents-and-space.html
- https://localhost:9443/space/widget-space-data-meet-sip.html
- https://localhost:9443/space/widget-space-data-meet-sip.html?sip=roomkit@sparkdemos.com
- http://localhost:9000/space/widget-space-data-spaceid.html?roomId=Y2lzY29zcGFyazovL3VzL1JPT00vNWU5YzM3YTAtMDFkOC0xMWU4LTg1NDgtMDFiYmYxOTZlZDNm
- http://localhost:9000/space/widget-space-data.html?email=CiscoDevNet@webex.bot

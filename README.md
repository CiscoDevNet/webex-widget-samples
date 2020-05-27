# Webex Teams Widgets Samples

[Webex Teams Widgets](https://developer.webex.com/docs/widgets) are open-source React components that let you integrate Cisco Webex Messaging & Audio/Video into your web apps.

If you're new to Widgets, we recommend you try the [Space Widget demo](https://code.s4d.io/widget-space/latest/demo/index.html).

This repository gathers simple examples to start with the 'Space' and 'Recents' widgets.



## Quickstart using hard-coded tokens (or passed as query parameters)

Enter the 'static' directory, and update each example with a Cisco Webex Teams API access token, or add `?token=XXXX` as a query parameter.

Then simply open the html file on your local machine in Chrome or Firefox.

Examples: 

Go to the static folder and open HTML file such as:

- file://.../static/space/widget-space-data.html?token=XXXXXXXXXXXXXXXXXXXXXXXXX
- file://.../static/recents/widget-recents-global.html?token=XXXXXXXXXXXXXXXXXXXXXXXXX
- file://.../static//together/both-recents-and-space.html?token=XXXXXXXXXXXXXXXXXXXXXXXXX
- file://.../static/space/widget-space-data.html?email=toEnglish@webex.bot
- file://.../static/space/widget-space-data-meet-sip.html?sip=fireplace@ivr.vc
- file://.../static/space/widget-space-data-spaceid.html?roomId=Y2lzY29zcGFyazovL3VzL1JPT00vNWU5YzM3YTAtMDFkOC0xMWU4LTg1NDgtMDFiYmYxOTZlZDNm


## Quick start on Glitch

Click [![Remix on Glitch](https://cdn.glitch.com/2703baf2-b643-4da7-ab91-7ee2a2d00b5b%2Fremix-button.svg)](https://glitch.com/edit/#!/import/github/CiscoDevNet/webex-widget-samples)


## Using Caddy: dynamically inject access tokens

Using [Caddy template actions](https://caddyserver.com/docs/template-actions), it's possible to customize the samples by injecting your own token (with the `ACCESS_TOKEN` env variable) and query parameters on the URL (`?roomId=`, `?sip=`, `?email=`). Read instructions below.

Download caddy: https://caddyserver.com/download, and add the command to your path.

Run the commands below from bash shell, and access the samples at ':9000/' (and ':9443/' for HTTPS access):

```bash
git clone https://github.com/CiscoDevNet/webex-widget-samples
cd webex-widget-samples
cd caddy
# Starts caddy with a Cisco Webex Teams API access token (check https://developer.webex.com)
ACCESS_TOKEN=access_token  caddy
```

Examples:

- http://localhost:9000/space/widget-space-data.html?email=toEnglish@webex.bot
- https://localhost:9443/space/widget-space-data-meet-sip.html?sip=fireplace@ivr.vc
- http://localhost:9000/space/widget-space-data-spaceid.html?roomId=Y2lzY29zcGFyazovL3VzL1JPT00vNWU5YzM3YTAtMDFkOC0xMWU4LTg1NDgtMDFiYmYxOTZlZDNm
- http://localhost:9000/recents/widget-recents-global.html
- http://localhost:9000/together/both-recents-and-space.html

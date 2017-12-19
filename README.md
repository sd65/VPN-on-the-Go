# VPN on the Go

VPN as a service on AWS.

## How to deploy

Click here :

[![Launch Stack](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png)](https://console.aws.amazon.com/cloudformation/home?region=eu-central-1#/stacks/new?stackName=VPNOnTheGo&templateURL=https://raw.githubusercontent.com/sd65/VPN-on-the-Go/master/main.template.yaml)

You have two parameters to enter:

* pVpnIpsecPsk: A secret pre-shared key used in IPsec/L2PT
* pVpnOnTheGoWebsitePassword: A secret password to access the VPNOnTheGo Website (and API)


## How to use

Wait for the stack to complete, open its Output tab and note the VpnOnTheGo URL.
Then simply visit this URL when you want to use this service.

At each visit you have to enter the pVpnOnTheGoWebsitePassword to login then you can create a new VPN or view existing ones.

## How to connect

First, for each VPN instance, 10 users are created:

* vpnonthego0
* vpnonthego1
* vpnonthego2
* ...
* vpnonthego9

The password is the same for those 10 users, it's displayed on the Website for this VPN instance.

When a new VPN is up, you can use it with multiple VPN protocols:

* OpenVPN (recommended for PC): Download the related config file and launch it with an OpenVPN Client. Simply input an username/password as explained above.
* IPsec/L2PT: Enter the IP and PSK you those earlier. Then sinply input an username/password as explained above.

## Costs

Not much.

## FAQ

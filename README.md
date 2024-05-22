# References

## Table Of Contents
1. [Create code.level.up Local Repo](#create-codelevelup-local-repo)
1. [Create Secured RDP Gateway Ubuntu](#create-secured-rdp-gateway-ubuntu)

## Create code.level.up Local Repo
1.  Log into your account at: https://code.levelup.cce.af.mil/
2.  Create access token:
    - goto Preferences > Access Tokens > Add new token
    - give token a name, select scopes, then create personal access token.
    - save your access token (you won't see it again and need it when you clone the repo)
3. Clone repository:
    - git -c http.sslVerify=false clone <http://path/to/repo>
    - change directory into repository
    - git config http.sslVerify "false"

## Create Secured RDP Gateway Ubuntu
Purpose: This section contains resources for creating a RDP gateway using Apache Guacamole, then creating a secured tunnel using CloudFlare using Ubuntu.

1. Create RDP Gateway using Apache Guacamole Ubuntu: [Click Here](https://www.atlantic.net/dedicated-server-hosting/how-to-create-remote-desktop-gateway-via-apache-guacamole-on-ubuntu-22-04/)

2. Create cloudflare account: [Click Here](https://www.cloudflare.com/)
3. Add site to cloudflare: [Click Here](https://developers.cloudflare.com/fundamentals/setup/manage-domains/add-site/)
4. Change your nameservers: [Click Here](https://developers.cloudflare.com/dns/zone-setups/full-setup/setup/)
5. Set up a tunnel through the dashboard: [Click Here](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/get-started/create-remote-tunnel/)


## Install Plesk

make sure open or allow port 80, 443, 8443, 8447, 8880

**Ubuntu 20.04**
```bash
  sudo apt update && sudo apt install -y curl wget
  sh <(curl https://autoinstall.plesk.com/one-click-installer || wget -O - https://autoinstall.plesk.com/one-click-installer)
```

if 'Installation is finished' follow the instructions in your terminal

## Install Node.js On Plesk

Log in to Plesk -> `Tools and Settings` -> `Updates` -> `Add/Remove Components` -> `Web hosting` -> `NodeJS support` -> `Continue`

## Domain

- Log in to Plesk -> `Websites & Domains` -> `Add Domain` -> `Blank website`
- input your domain -> `Add Domain` 
- add A DNS RECORDS

| Type      | Name     | Value                      |
| :-------- | :------- | :------------------------- |
| A         | @        | your server IPv4 address   |
| A         | www      | your server IPv4 address   |

## Subdomain

- Log in to Plesk -> `Websites & Domains` -> `Add Subdomain` -> `Blank website`
- input your subdomain -> `OK` 
- add A DNS RECORDS

| Type      | Name      | Value                      |
| :-------- | :-------  | :------------------------- |
| A         | subdomain | your server IPv4 address   |

**once you have finished setting up your domain or subdomain, you can access your domain and you will see the default plesk page**

## Setup Node.js App

- Log in to Plesk -> `Websites & Domains` -> `Click between domain or subdomain` -> `Dashboard` -> `Create Website` -> `Node.js`
- select `Package Manager` to npm
- in the `Application Root`, click the `/` symbol and select where you extracted the script either in httpdocs or a subdomain
- `Enable Node.js` -> `NPM install` - `Run script`

## SSL

- Log in to Plesk -> `Websites & Domains` -> `Click between domain or subdomain` -> `Dashboard` -> `SSL/TLS Certificates` -> `Install a free basic certificate provided by Let's Encrypt` -> `Install` -> `check all options` -> `Get it free`
- follow the instructions

**Once you have finished following the instructions provided, please try reloading your domain or subdomain, SSL should be installed.**


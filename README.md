nginx-plex-deluge-proxy
=======================

This is an NGINX configuration to allow plex and deluge reverse proxy.

It gives you the following paths:

* `https://X.X.X.X/plex`
* `https://X.X.X.X/deluge`

## Installation

### Step 1

These files need to be copied/cloned into the NGINX config folder, for example `/etc/nginx` on Ubuntu.

### Step 2

You then need to generate self signed SSL certificate:

```bash
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout media_proxy/ssl/nginx.key -out media_proxy/ssl/nginx.crt
```

### Step 3

Create `media_proxy/htpasswd` file using [this handy site](http://www.htaccesstools.com/htpasswd-generator/) or native means, whatever you feel comfortable with. This username/password will be prompted for when you try to access the proxy.



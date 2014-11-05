nginx-plex-deluge-proxy
=======================

This is an NGINX configuration to allow plex and deluge reverse proxy.

It gives you the following paths:

* `http://X.X.X.X/` -> plex
* `http://X.X.X.X/deluge`
* `http://X.X.X.X/couchpotato`

On my laptop, I edited `/etc/hosts` to include `X.X.X.X media` so that I can type `http://media` instead of IP.

## Installation

### Step 1

These files need to be copied/cloned into the NGINX config folder, for example `/etc/nginx` on Ubuntu.

### Step 2

Create `media_proxy/htpasswd` file using [this handy site](http://www.htaccesstools.com/htpasswd-generator/) or native means, whatever you feel comfortable with. This username/password will be prompted for when you try to access the proxy.

### Step 3

Restart NGNIX `sudo service nginx restart`

### Step 4

You should be able to open `http://X.X.X.X` and see Plex now.


A script to set up SOCKS5 proxy. Can be used for Telegram.
Tested on [Digital Ocean droplet](http://www.digitalocean.com/?refcode=a2c0ba080f43).

1. Create ansible inventory named "hosts", use "hosts.template"
2. Create user list ".proxyauth" using ".proxyauth.template" or just leave as-is to configure later.
3. Run:
ansible-playbook proxy.yml -i hosts
4. Connect to host:50228

Optianally edit user list later:
/etc/3proxy/.proxyauth
After editing don't forget to restart srvice:
systemctl restart 3proxy.service

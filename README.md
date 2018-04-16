1. Create ansible inventory named "hosts", use "hosts.template"
2. Create user list ".proxyauth" using ".proxyauth.template" or just leave as-is to configure later.
3. Run:
ansible-playbook proxy.yml -i hosts

Optianally edit user list later:
/etc/3proxy/.proxyauth
After editing don't forget to restart srvice:
systemctl restart 3proxy.service
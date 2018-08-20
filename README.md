Fail2Ban Action Configuration for CloudFlare REST API V4
========================================================

Note: _This will only work if you have full access to your web server's `/etc/fail2ban/` files._

Installation:

* Copy [action.d/cloudflare-restv4.conf](https://github.com/wpkc/fail2ban-action-cloudflare-restv4/blob/master/action.d/cloudflare-restv4.conf) to your `/etc/fail2ban/action.d` directory.
* Get your CloudFlare Global API Key at: <https://dash.cloudflare.com/profile>
* Modify your `/etc/fail2ban/jail.local` as shown in the sample [jail.local](https://github.com/wpkc/fail2ban-action-cloudflare-restv4/blob/master/jail.local) file provided in this repository. Set `cfemail` and `cfapikey` to your cloudflare account email and Global API Key respectively.
* Restart Fail2Ban with: `service fail2ban restart`
* Please consider using [mod_cloudflare](https://github.com/cloudflare/mod_cloudflare) on Apache2 servers to make sure you are using the correct IP address as the client IP address.

More info: <https://www.kazimer.com/fail2ban-action-for-cloudflare-rest-api-v4/>

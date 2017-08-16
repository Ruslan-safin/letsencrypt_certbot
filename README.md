# README #

### Deploy NGINX and LetsEncrypt with Certbot ###

* Version 16.06.26

### How do I get set up? ###

* Install nginx: `apt-get install -y nginx`
* Copy config files`
* Download Certbot: `wget https://dl.eff.org/certbot-auto`
* Change permissions: `chmod a+x certbot-auto`
* Run Certbot: `./certbot-auto`
* Use the certonly command to obtain your certificate: `./opt/certbot/certbot-auto certonly`
* To automating renewal: `./opt/certbot/certbot-auto renew --dry-run`
* To use with cron or systemd job: `./opt/certbot/certbot-auto renew --quiet --no-self-upgrade`
* To add Cron task: `crontab -e` and paste `@daily /opt/certbot/renewCerts.sh`
* Make renewCerts.sh executable: `chmod +x /opt/certbot/renewCerts.sh`
* Restart Nginx service: `service nginx restart`
* SSL Server Test: `https://www.ssllabs.com/ssltest/`
* Analyze HTTP Response Headers: `https://securityheaders.io`

### Who do I talk to? ###

* Repo owner CyberManiac

# Setup Commands

## 1. Apache Web Server

sudo apt update
sudo apt install apache2 -y
sudo systemctl enable --now apache2

## 2. Splunk Log Ingestion
# Add splunk user to adm group
sudo usermod -aG adm splunk

# Restart Splunk
sudo /opt/splunk/bin/splunk restart

# Add Apache log monitor
sudo /opt/splunk/bin/splunk add monitor /var/log/apache2/access.log -index main -sourcetype apache:access

## 3. Generate Test Attacks
curl http://127.0.0.1/phpmyadmin
curl http://127.0.0.1/?test=../../../etc/passwd
curl http://127.0.0.1/.env

## 4. Restart Services
sudo systemctl restart apache2
sudo /opt/splunk/bin/splunk restart
docker-compose up -d   # In ~/Downloads/shuffle/Shuffle

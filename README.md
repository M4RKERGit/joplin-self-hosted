# Joplin for self-hosting without domain name

### Fast setup for self-hosted Joplin for server without domain name

1. Clone this repo with ```git clone https://github.com/M4RKERGit/joplin-self-hosted.git```
2. Edit docker-compose.yaml and put here your PG DB password and dummy domain
3. Edit ./nginx/joplin-sync and put dummy domain and your server ip here
4. Copy ./nginx/joplin-sync to /etc/nginx/sites-enabled/
5. Run ```docker compose up -d```
6. Connect your Joplin clent via Sync Wizard, set URL=http://{SERVER_IP}:9000, email=admin@localhost, password=admin
7. Enjoy)

P.S. IDK why but if i copy ONLY joplin-sync conf, nginx won't redirect my requests, so i copying whole /etc/nginx directory #FIXME
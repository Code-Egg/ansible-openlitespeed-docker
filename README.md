# Ansible Playbook for setting up OpenLiteSpeed Docker environment

## How to use
1. Install ansible on center server
```
apt update && apt install ansible -y
```
2. Add SSH key to the client server so center server can ssh in without password
3. Download the git repo
```
git clone https://github.com/Code-Egg/ansible-openlitespeed-docker.git
```
4. Update `example.com` from inventory to your client server's domain/IP
```
cd ansible-openlitespeed-docker; vi inventory
```
5. Run ansible playbook
```
ansible-playbook playbook.yml
```

## Next
Your client server now should has `docker`, `docker-compose` installed and https://github.com/litespeedtech/ols-docker-env downloaded to /opt/openlitespeed-docker. 
Open a terminal, cd to the folder `/opt/openlitespeed-docker` in which docker-compose.yml is saved, and run:
```
docker-compose up -d
```
123
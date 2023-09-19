# PostgreSql-Streaming-replication
![diagram](Capture.PNG)


#  Ubuntu 22.04 Server on PostgreSQL-14 Installation Guide Step by Step Procedure

First, update and upgrade your system and check if a reboot is required:

```shell
sudo apt update && sudo apt -y full-upgrade
```
```
[ -f /var/run/reboot-required ] && sudo reboot -f
```

 Then, install the required dependencies:
```
sudo apt install vim curl wget gpg gnupg2 software-properties-common apt-transport-https lsb-release ca-certificates
```
Check the policy for PostgreSQL:
```
apt policy postgresql
```
Add the PostgreSQL GPG key to trusted keys:
```
curl -fsSL https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/postgresql.gpg
```
Add the PostgreSQL repository:
```
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
```
Update the package list:
```
sudo apt update
```
Install PostgreSQL 14:
```
sudo apt install postgresql-14
```
Check the status of the PostgreSQL service:
```
systemctl status postgresql@14-main.service
```





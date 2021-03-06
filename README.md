[![Mage4](http://www.mage4.com/wp-content/uploads/2019/10/Asset-1-1.png)]()

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)
# Using Instructions
Clone the repo, switch to required magento branch  and clone or move project in src
forlder in current directory. If fresh magento installation is required create auth.json file with magento credentials in ~/.composer/ folder and run below command to download the magento in src folder.

```sh
bin/download 2.3.5
```
where 2.3.5 could be any version but you should be in compatable branch to make it work properly.
In src folder rename nginx.conf.sample to nginx.conf.
Configure database environment params in  env/db.env file.
Append app host domain name in name resolver file using below command

```sh
echo "127.0.0.1 ::1 $DOMAIN" | sudo tee -a /etc/hosts
```
Install Magento using below command 
```sh
bin/setup $DOMAIN
```
replace $DOMAIN with you required domain name.

Now launch the docker environment 
```sh
docker-compose up
```
If you want to switch enivronment you first need to pull down current running environemnt.
```sh
docker-compose down
```

# Contribution Instructions
Checkout from main branch with the branch name along with magento version you required. (i.e magento-scandiwebpwa-2.3.5). Make necessary changes in docker files to meet the technology stack requirements. Push your branch.

| Note: Never merge your branch in main branch as every branch is independently used.   |
| --- |

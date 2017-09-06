# rabbitmq

Please find the steps below to execute on three os families:

Ubuntu

curl -L https://www.opscode.com/chef/install.sh | bash

chef-solo -v

cd /root

git clone https://github.com/Anuj1990/rabbitmq.git 

mv rabbitmq chef-repo 

cd /root/chef-repo

cp ca* /etc/ssl

cp cert* /etc/ssl

chef-solo -c solo.rb -j run.json 



CentOS

curl -L https://www.opscode.com/chef/install.sh | bash

chef-solo -v

cd /root

git clone https://github.com/Anuj1990/rabbitmq.git 

mv rabbitmq chef-repo 

cd /root/chef-repo

cp ca* /etc/ssl

cp cert* /etc/ssl

chef-solo -c solo.rb -j run_amazon.json


RHEL

curl -L https://www.opscode.com/chef/install.sh | bash

chef-solo -v

cd /root;

git clone https://github.com/Anuj1990/rabbitmq.git 

mv rabbitmq chef-repo 

cd /root/chef-repo

cp ca* /etc/ssl

cp cert* /etc/ssl

chef-solo -c solo.rb -j run_rhel.json

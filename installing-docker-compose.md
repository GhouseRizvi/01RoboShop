

You can start from the scratch on Amazon Linux ec2 instance for installing Docker by following the step:

sudo yum update -y 

sudo amazon-linux-extras install docker 

sudo yum install docker 

sudo service docker start 

sudo usermod -a -G docker ec2-user 

Then logout from the instance and login again to verify the installation of Docker

docker info 

To install Docker-compose follow the below steps:

sudo curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

docker-compose version


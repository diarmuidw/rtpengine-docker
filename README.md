[![Build Status](https://travis-ci.org/ReadyTalk/rtpengine-docker.svg?branch=master)](https://travis-ci.org/ReadyTalk/rtpengine-docker)

# RTPEngine Docker

A Docker container for running rtpengine.  This is meant to be used next to Kamailio for a WebRTC SIP Proxy.  It is largely based on the projects listed in the references.

Uses Ubuntu 18.04.1 LTS as host in EC2

## References (and Credit)
https://github.com/ianblenke/docker-rtpengine

https://github.com/havfo/WEBRTC-to-SIP

https://github.com/sipwise/rtpengine

## Instructions AWS

Use Ubuntu 18.04 as that is supported by Docker CE

sudo apt-get update

sudo apt-get install -y \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
	
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
   
sudo apt-get update

sudo apt-get install -y docker-ce docker-ce-cli containerd.io

sudo docker run hello-world


 mkdir Readytalk
 
 cd Readytalk/
 
 git clone https://github.com/diarmuidw/rtpengine-docker.git
 
 cd rtpengine-docker/
 
 docker build -t dwrtpengine .
 
 #make tea
 
 chmod +x docker_run.sh

./docker_run.sh

#ignore error on rm command
 
 netstat -tulpn
 
 confirm lots of services running
 
 apt-get install ngrep

 ngrep -p -q -W byline port 22222
 
 You should see nothing much until Kamalio is configured to send traffic to this
 
 

 
 

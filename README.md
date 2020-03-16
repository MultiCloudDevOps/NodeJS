
## Install NodeJS server with sample application using dockerfile #


- Pre-requisites 

  `OS : Ubuntu 16.04`

- Install docker if docker is not installed. 

  `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -` <br />
  `sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"`<br />
  `sudo apt-get update`

- Install docker community edition

  `apt-cache policy docker-ce` <br />
  `sudo apt-get install -y docker-ce` <br />

  `sudo systemctl status docker`

- Build your nodejs docker image with dockerfile, nodejs samples application 

  `docker build -t <your username>/node-web-app .` <br />

  `docker images`     # to view newly created nodejs docker image.  <br />
  
  `docker run -p 49160:8080 -d <your username>/node-web-app`    # 49160 external access, 8080 internal access for nodejs.` <br />
  
  `curl -i localhost:49160`


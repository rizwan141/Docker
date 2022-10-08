# Docker

### How to install Docker ?
##### Install Docker on Ubuntu : PROD
###### A. Set up the repository
1. Update the apt package index and install packages to allow apt to use a repository over HTTPS
```
sudo apt-get update
```
```
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```
2. Add Docker’s official GPG key
```
sudo mkdir -p /etc/apt/keyrings
```
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```
3. Use the following command to set up the repository
```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
###### B. Install Docker Engine

* Update the apt package index, and install the latest version of Docker Engine, containerd, and Docker Compose
```
sudo apt-get update
```
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```
###### C. Verify that Docker Engine is installed correctly by running the hello-world image (optional)
```
sudo service docker start
```
```
sudo docker run hello-world
```
###### to verify the docker version use ```docker version``` CMD
###### for socket error give the executable permission ```sudo chmod 777 /var/run/docker.sock```
<img width="1439" alt="Screenshot 2022-10-08 at 4 20 55 PM" src="https://user-images.githubusercontent.com/103893307/194703847-e6b50338-eb2b-4ff5-959f-9f3bdae725c4.png">


##### Install Docker on Ubuntu With Single Line Command : POC

```sudo apt  install docker.io```  # version 20.10.12-0ubuntu2~20.04.1
### Deploy Any application using Cloud Native Builpacks

#### Pre-requisites:

- AWS account
- An Ubuntu EC2 machine t2.micro (t2.micro is ok, if you are using simple application)
- Docker installed

#
#### Steps:
- Update your machine
```bash
sudo apt update
```
#
- Install docker
```bash
sudo apt install docker.io -y
```
#
- Provide permission to ubuntu user to docker group
```bash
sudo usermod -aG docker $USER && newgrp docker
```

#
- Install pack utility to build image
```bash
sudo add-apt-repository ppa:cncf-buildpacks/pack-cli
sudo apt-get update
sudo apt-get install pack-cli
```
#
- Clone your code
```bash
git clone https://github.com/DevMadhup/node-todo-cicd.git
```
#
- Go inside the directory
```bash
cd node-todo-cicd
```
#
- Remove Dockerfile and docker-compose file to make sure we are not using it for building the image.
```bash
rm -rv Dockerfile
rm -rv docker-compose.yaml
```
#
- Run the following command to get the pack builder
```bash
pack build suggest
```
#
- Copy the google builder and paste in the below command
```bash
pack build --builder=<your-builder-from-above-command> node-app
```

<img width="894" alt="image" src="https://github.com/user-attachments/assets/33e00d6d-0a98-4e16-9783-e07b7a155459">
> [!Note]
> This build will take some time be patient.

#
- After build, check images
```bash
docker images
```
#
- Run the image as a container
```bash
docker run -itd --name nodeapp -p 8000:8000 node-app
```
> [!Note]
> This application runs on port 8000, that's why we mentioned 8000 in the above command
#
- Open port 8000 from the security groups and access your application
```bash
http://<public-ip>:8000
```
#
Congratulations!!! you have deployed and application using Cloud Native Buildpacks.

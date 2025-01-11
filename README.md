# Installation
This repository for the different software, tools and components installation in easy words


# How To Install and Use Docker on Ubuntu
## Step 1 — Installing Docker
The Docker installation package available in the official Ubuntu repository may not be the latest version. To ensure we get the latest version, we’ll install Docker from the official Docker repository. To do that, we’ll add a new package source, add the GPG key from Docker to ensure the downloads are valid, and then install the package.
First, update your existing list of packages:
``` bash
sudo apt update
```
Next, install a few prerequisite packages which let apt use packages over HTTPS:
``` bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```
Then add the GPG key for the official Docker repository to your system:
``` bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
Add the Docker repository to APT sources:
``` bash
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
Update your existing list of packages again for the addition to be recognized:
``` bash
sudo apt update
```

The second step.
Install Docker environment.

## Task

1. Update the apt package index and install packages to allow apt to use a repository over HTTPS:

   `apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common`{{execute}}

2. Add Docker’s official GPG key:
   `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -`{{execute}}

3. Update the apt package index, 
   `apt-get update`{{execute}}
4. Install the latest version of Docker Engine and containerd, or go to the next step to install a specific version:
   `apt-get install docker-ce docker-ce-cli containerd.io`{{execute}}

5. Run this command to download the current stable release of Docker Compose:
   `curl -L "https://github.com/docker/compose/releases/download/1.26.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`{{execute}}
6. Apply executable permissions to the binary:
   `chmod +x /usr/local/bin/docker-compose`{{execute}}

## Verify docker installation

7. Test the installation Docker-ce
   `docker version`{{execute}}
8. Test the installation Docker Compose
   `docker-compose --version`{{execute}}
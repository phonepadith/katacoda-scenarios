This is first step.
Install Docker environment.

## Task

1. update Linux
`sudo apt-get update`{{execute}}

2. Update the apt package index and install packages to allow apt to use a repository over HTTPS:

`sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common`{{execute}}

3. Add Docker’s official GPG key:
`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`{{execute}}


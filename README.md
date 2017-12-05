# environment

# Nicer terminal
https://github.com/robbyrussell/oh-my-zsh
- sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
Use .zshrc instead .bashrc for adding stuff.

# Guthub token
- go to github
- go to profile settings
- go to developper stuff
- generate github token
- copy token
- edit .bashrc: export GITHUB_TOKEN=*paste token here*

# Docker
https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/
- remove previous install: `sudo apt-get remove docker docker-engine docker.io`
- update `sudo apt-get update`
- run `sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common`
- add repo: `url -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`
- update: `sudo apt-get update`
- install: `sudo apt-get install docker-ce`

If nothing happens, eg: for new distrib, find .deb file: eg for Artful https://download.docker.com/linux/ubuntu/dists/artful/pool/ in the *edge* directory

# Docker compose
https://docs.docker.com/compose/install/#install-compose
- run `sudo curl -L https://github.com/docker/compose/releases/download/1.17.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose`
- run `sudo chmod +x /usr/local/bin/docker-compose`
- test by running `docker-compose --version`

# Docker without root privileges
https://docs.docker.com/engine/installation/linux/linux-postinstall/
- run `sudo groupadd docker`
- run `sudo usermod -aG docker MyUserName`
- log out and log back in
- test `docker run hello-world`




# Setup_Freqtrade_Docker_image_Installation
First I prefer to make a new directory called `/opt` because we are going to Add-on application software packages.

- Creating a new directory called /opt is preferred because it allows for the addition of application software packages that are not part of the default Ubuntu package repositories. This directory is commonly used to store software and programs that are not installed through the package manager.

## _Docker quick start_
``` bash
mkdir ft_userdata
cd ft_userdata/
# Download the docker-compose file from the repository
curl https://raw.githubusercontent.com/freqtrade/freqtrade/stable/docker-compose.yml -o docker-compose.yml

# Pull the freqtrade image
docker compose pull

# Create user directory structure
docker compose run --rm freqtrade create-userdir --userdir user_data

# Create configuration - Requires answering interactive questions
docker compose run --rm freqtrade new-config --config user_data/config.json
```

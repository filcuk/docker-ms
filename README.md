# docker-ms
Basic Docker media server template

# Steps
## RPi Setup
1. Install OS on a microSD using [Raspberry Pi Imager](https://www.raspberrypi.com/software/)  
  *You can configure net SSH access and network before installation.*
1. SSH into the RPi: `ssh 192.168.x.x@user`  
  *You can run `sudo raspi-config` to finish setting up your device.*

## Docker Setup
1. Update RPi: `sudo apt update && sudo apt upgrade`
1. Run Docker setup: `curl -sSL https://get.docker.com | sh`  
  *Typically not recommended, but Docker is a trusted source.*
1. Add user to the Docker group: `sudo usermod -aG docker [user]`  
  Or `sudo usermod -aG docker ${USER}` to add current user
  *You can check it running `groups ${USER}`.*
1. Restart to apply changes: `sudo restart`
1. SSH to the RPi again

## Compose Setup
This is an optional step, but recommended.
1. Install `pip3`:   
  *`python3` & `pip3` are required to setup and run `docker-compose`.*
  ```bash
  sudo apt-get install libffi-dev libssl-dev
  sudo apt install python3-dev
  sudo apt-get install -y python3 python3-pip
  ```
1. Install `docker-compose`: `sudo pip3 install docker-compose`

## Environment Setup


## Launch

# DemoRep
**Step 1. Download and install Ubuntu on VirtualBox**

  [Official website](https://ubuntu.com/)

**Step 2. Install Docker**

  Prerequisites
  ```
  # update existing list of packages
  sudo apt update 
  # install prerequisites
  sudo apt install apt-transport-https ca-certificates curl software-properties-common
  # add GPG key for the official Docker repo to system
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - 
  # add the Docker repo to apt sources
  sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
  ```
  Installation
  ```
  # install from the Docker repo
  apt-cache policy docker-ce
  # install Docker
  sudo apt install docker-ce 
  # check that Docker is running
  sudo systemctl status docker 
  ```
  Additional
  ```
  # add username to the docker group to use docker commands without sudo
  sudo usermod -aG docker ${USER} 
  ```

**Step 3. Run the jupyter notebook**
  
  ```
  docker pull jupyter/datascience-notebook
  docker run -p 8888:8888 -v $(pwd):/home/user/ds jupyter/datascience-notebook
  ```
  
  **Some notebooks**
  
  [Kaggle Titanic Competition](https://github.com/ktrlv/DemoRep/blob/main/Titanic/Titanic.ipynb)
  
  [Kaggle Spaceship Titanic Competition](https://github.com/ktrlv/DemoRep/blob/main/SpaceshipTitanic/SpaceshipTitanic.ipynb)

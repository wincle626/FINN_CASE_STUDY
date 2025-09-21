# FINN_CASES_STUDY

## 1. Install docker

### Add Docker's official GPG key:
`
sudo apt-get update
`

`
sudo apt-get install ca-certificates curl
`

`
sudo install -m 0755 -d /etc/apt/keyrings
`

`
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
`

`
sudo chmod a+r /etc/apt/keyrings/docker.asc
`

### Add the repository to Apt sources:
`
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
`

`
sudo apt-get update
`

`
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
`

`
sudo systemctl status docker
`

`
sudo systemctl start docker
`

`
sudo docker run hello-world
`


## 2. Install from finn repository

`
python3 -m venv pyvenv
`

`
source pyvenv/bin/activate
`

`
git clone https://github.com/Xilinx/finn.git
`

`
cd finn
`

`
pip install -r requirements.txt
`

`
export VITIS_PATH=/tools/Xilinx/Vitis/2024.1
`

`
export VIVADO_PATH=/tools/Xilinx/Vivado/2024.1
`

## 3. Test finn example repository

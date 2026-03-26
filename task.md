# Quick Tasks

## What to Do

- [ ] Deploy the serverless image processor with Lambda and S3
- [ ] Upload test images and verify all 5 variants are generated
- [ ] Write a short blog (800-1000 words) about your implementation
  - Include architecture diagram showing S3 → Lambda → S3 flow
  - Add screenshots of deployment and processed images
  - Document Lambda layers and serverless architecture
     
  - https://awspolicygen.s3.amazonaws.com/policygen.html (AWS Policy generator)
     
- [ ] Install Terraform
      - sudo apt update && sudo apt upgrade -y
      - sudo apt install -y gnupg software-properties-common curl
      - curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
      - sudo apt-add-repository "deb https://apt.releases.hashicorp.com $(lsb_release -cs) main"
      - sudo apt update
      - sudo apt install terraform -y
      - terraform -version

- OR 
wget https://releases.hashicorp.com/terraform/1.7.5/terraform_1.7.5_linux_amd64.zip
unzip terraform_1.7.5_linux_amd64.zip
sudo mv terraform /usr/local/bin/


- Install Docker

  sudo apt update && sudo apt upgrade -y
  sudo apt install -y ca-certificates curl gnupg lsb-release

  sudo mkdir -p /etc/apt/keyrings

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

sudo systemctl start docker
sudo systemctl enable docker

docker --version
sudo usermod -aG docker $USER
newgrp docker
exit
docker ps



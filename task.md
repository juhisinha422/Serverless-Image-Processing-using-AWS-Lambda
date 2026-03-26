# 🚀 Serverless Image Processing using AWS Lambda

## 📌 Overview

This project implements a **serverless image processing pipeline** using AWS services. When an image is uploaded to an S3 bucket, an AWS Lambda function is automatically triggered to process the image and generate multiple resized variants.

---

## 🏗️ Architecture

```
S3 (Upload Bucket) → Lambda Function → S3 (Processed Images)
```

* **Amazon S3**: Stores original and processed images
* **AWS Lambda**: Processes images and generates variants
* **IAM Roles & Policies**: Secure access between services

---

## ✨ Features

* 📸 Automatic image processing on upload
* 🖼️ Generates **5 image variants**
* ⚡ Event-driven architecture using S3 triggers
* ☁️ Fully serverless and scalable
* 🧱 Infrastructure as Code using Terraform

---

## 🛠️ Tech Stack

* AWS Lambda
* Amazon S3
* Terraform
* Docker
* IAM

---

## 📁 Project Structure

```
.
├── assets/                # Screenshots and architecture diagrams
├── lambda/                # Lambda function code
├── scripts/               # Helper scripts
├── terraform/             # Infrastructure as Code
├── Implementation.txt     # Implementation notes
├── README.md              # Project documentation
└── task.md                # Assignment tasks
```

---

## ⚙️ Setup & Installation

### 🔹 Install Terraform

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y gnupg software-properties-common curl
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
sudo apt-add-repository "deb https://apt.releases.hashicorp.com $(lsb_release -cs) main"
sudo apt update
sudo apt install terraform -y
terraform -version
```

### 🔹 Alternative (Manual Install)

```bash
wget https://releases.hashicorp.com/terraform/1.7.5/terraform_1.7.5_linux_amd64.zip
unzip terraform_1.7.5_linux_amd64.zip
sudo mv terraform /usr/local/bin/
terraform -version
```

---

### 🔹 Install Docker

```bash
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
```

### 🔹 Run Docker without sudo

```bash
sudo usermod -aG docker $USER
newgrp docker
```

---

## 🚀 Deployment Steps

### 1️⃣ Initialize Terraform

```bash
cd terraform
terraform init
```

### 2️⃣ Plan Infrastructure

```bash
terraform plan
```

### 3️⃣ Deploy Resources

```bash
terraform apply
```

---

## 🧪 Testing

1. Upload an image to the S3 input bucket
2. Lambda function triggers automatically
3. Verify output bucket for **5 processed images**

---

## 🔐 IAM Policy

Use AWS Policy Generator:
https://awspolicygen.s3.amazonaws.com/policygen.html

Ensure permissions:

* S3 read/write
* Lambda execution

---

## 📝 Blog Requirement

* Architecture diagram (S3 → Lambda → S3)
* Screenshots of deployment
* Processed image outputs
* Explanation of Lambda layers
* Key learnings and challenges

---

## 💡 Key Learnings

* Serverless architecture design
* Event-driven systems (S3 → Lambda)
* Infrastructure as Code using Terraform
* Docker for dependency packaging

---

## 🚀 Future Enhancements

* API Gateway integration
* CI/CD pipeline using GitHub Actions
* Image format conversion
* Monitoring with AWS CloudWatch

---

## 📬 Conclusion

This project demonstrates a **real-world serverless architecture** using AWS, enabling automated, scalable, and efficient image processing without managing servers.

---

## ⭐ Support

If you found this project helpful, consider giving it a ⭐ on GitHub!

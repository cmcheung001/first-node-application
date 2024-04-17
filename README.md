# first-node-application
first-node-application on 20240415 and 20240417 for 3.3, 3.4 and 3.5

*** 4 commands to build and upload docker image into AWS ECR
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 255945442255.dkr.ecr.us-east-1.amazonaws.com

docker build -t jeremy-node-docker-20240417 .

docker tag jeremy-node-docker-20240417:latest 255945442255.dkr.ecr.us-east-1.amazonaws.com/jeremy-node-docker-20240417:V1

docker push 255945442255.dkr.ecr.us-east-1.amazonaws.com/jeremy-node-docker-20240417:V1   


*** run the docker image locally

docker run -p 8080:3000 255945442255.dkr.ecr.us-east-1.amazonaws.com/jeremy-node-docker-20240417:V1








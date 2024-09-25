# NodeJS Express Image

## Install NodeJS
```bash
choco install nodejs-lts --version="20.17.0"
node -v
cd nodejs-express/app
npm init -y
```

## Authenticate with Docker

```bash
aws ecr get-login-password --region ap-southeast-5 | docker login --username AWS --password-stdin 202533527371.dkr.ecr.ap-southeast-5.amazonaws.com
```

## Build the Image

```bash
docker build --tag nodejs-express ./app
```

## Push the Image to ECR

```bash
docker images
docker tag <id> 202533527371.dkr.ecr.ap-southeast-5.amazonaws.com/nodejs-express:latest
docker push 202533527371.dkr.ecr.ap-southeast-5.amazonaws.com/nodejs-express:latest
```

## Test the Image

```bash
docker run -d -p 3000:3000 nodejs-express
```
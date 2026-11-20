# Project 13: Build Image and Push to ECR

## Objective
Build a Docker image and publish it to Amazon Elastic
Container Registry (ECR).

## Technologies Used
- Docker
- Nginx
- AWS CLI
- Amazon ECR
- Git
- GitHub

## Implementation
1. Created a simple Nginx web application.
2. Created a Dockerfile.
3. Built the Docker image locally.
4. Tested the application using Docker.
5. Created a private ECR repository.
6. Authenticated Docker with Amazon ECR.
7. Tagged and pushed the image to ECR.
8. Verified the uploaded image in AWS Console.

## Image Details
- Repository: project13-web-app
- Tag: v1
- AWS Region: ap-south-1

## Evidence
Screenshots showing Docker build, successful push,
and ECR image verification.

## Result
The Docker image was successfully pushed to Amazon
ECR and verified in the repository.

## ECR Push Verification

Successfully built and pushed the Docker image to Amazon Elastic Container Registry.

### Image Details

- **Repository:** project13-web-app
- **AWS Region:** ap-south-1
- **Image Tag:** v1
- **Image URI:** `590507089733.dkr.ecr.ap-south-1.amazonaws.com/project13-web-app:v1`

### Verification

Executed:

```bash
aws ecr describe-images \
  --repository-name project13-web-app \
  --image-ids imageTag=v1 \
  --region ap-south-1
```

The command confirmed that the image was successfully uploaded to ECR.

### Evidence

![Docker Build](screenshots/proj_13-docker-image-build.png)

![Docker Push Success](screenshots/proj13_02-docker-push-success.png)

![ECR Image Verification](screenshots/proj13_03-ecr-image-uploaded.png)

### Result

Successfully built, tagged, and published a Docker container image to a private Amazon ECR repository.

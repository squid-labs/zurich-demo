pipeline{
  agent any
  environment {
    AWS_ACCOUNT_ID="202533527371"
    AWS_DEFAULT_REGION="ap-southeast-5"
    CLUSTER_NAME="test-cluster"
    SERVICE_NAME="test-service"
    TASK_DEFINITION_NAME="test-app-task-family"
    DESIRED_COUNT="1"
    IMAGE_REPO_NAME="nodejs-server"
    IMAGE_TAG="${env.BUILD_ID}"
    REPOSITORY_URI="${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com/${IMAGE_REPO_NAME}"
    registryCredential = "1ada4568-9ead-44ee-b059-4ec8c84d99c1"
  }
}
Sagemaker Notebook instance:
The instance type chosen is ml.t3.medium as we don't have very high processing in notebooks and training jobs are run on seperate machines.

EC2 Instance:
the EC2 instance is chosen to run the training with Deep Learning AMI. The chosen EC2 isntance is ml.medium instance as we don't want to overshoot the cost for processing.

Lambda IAM issue:
The Lambda failed for the first run as seen in LamndaError>PNG due to insuffucient access. After the IAM policy was changed as per IAM.PNG, the Lambda run was success as seen in LambdaSuccess.PNG

Lambda Concurrency and Auto Scaling for endpoint:
The Lamda concurrency was configured to be 2 instances to handle multiple runs simuntaneously. 
The endpoint was scaled to also auto scale to 2 instances for heavy usage.
# Serverless-Emailing-Applications
AWS Email Automation Project
Overview
This project automates the process of sending personalized emails using AWS services. It integrates GitHub for source management, AWS S3 for storing email templates and contact information, AWS CodePipeline for continuous integration, AWS Lambda for executing scripts, and AWS SES for sending emails.

# Architecture
1. GitHub: Used for managing the source code, email templates, and contact files.

2. AWS S3: Stores email templates, email IDs, and names.

3. AWS CodePipeline: Connects GitHub with S3 to automatically update changes in the code.

4. AWS Lambda:
   * Triggers a Python script to send emails.
   * Extracts names from the contact file and personalizes the emails.
   * Uses a trigger function for timely email sending.
  
5. AWS SES: Sends the emails to the recipients automatically.
# Workflow
1. Source Code Management:

   * Email templates and contact files are maintained in a GitHub repository.
   
2. Storage:

   * Templates and contact details are uploaded to an S3 bucket.

3. Continuous Integration:

    * AWS CodePipeline monitors the GitHub repository.
    * On detecting changes, CodePipeline updates the S3 bucket with the latest templates and contact files.

4. Email Sending:

  * AWS Lambda is triggered by changes in the S3 bucket.

  * The Lambda function:
      * Reads the email template and contact file from S3.
      * Personalizes the email using the recipient's name from the contact file.
      * Sends the email using AWS SES.

5. Scheduled Emails:

   A trigger function in Lambda ensures emails are sent at scheduled times.
# Prerequisites
* AWS Account
* GitHub Account
* AWS CLI configured
* Necessary permissions to create and manage AWS services
# Setup Instructions
Clone the GitHub Repository:

git  clone 

cd repository-directory

# Setup S3 Bucket:

* Create an S3 bucket to store email templates and contact files.
* Upload the email template and contact file to the S3 bucket.
* 
#  Create AWS Lambda Function:

* Create a Lambda function to handle the email sending logic.
* Configure the function to trigger on S3 events (object creation) and on a scheduled basis.
# Configure AWS SES:

* Verify your email address with SES.
* Configure SES to allow sending emails.
# Setup AWS CodePipeline:

* Create a pipeline in AWS CodePipeline.
* Connect the pipeline to your GitHub repository and S3 bucket.
# CodePipeline Configuration

1. Source Stage:

Add a source stage to connect to the GitHub repository.

2. Deploy Stage:

Add a deploy stage to sync changes with the S3 bucket.

# Lambda Function
The Lambda function script (e.g., send_email.py) should:

1. Retrieve the email template and contact file from S3.
2. Extract names and email addresses from the contact file.
3. Personalize the email template.
4. Send the email using AWS SES.

![ddd](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20001141.png)
![dddd](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20003412.png)
![ggg](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20003704.png)
![ggg](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20003820.png)
![ggg](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20004409.png)
![ggg](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20004948.png)
![ggg](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20012435.png)
![ggg](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20013926.png)
![ggg](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20014050.png)
![ggg](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20022020.png)
![ggg](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20024120.png)
![ggg](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20024142.png)
![ggg](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20024515.png)
![ggg](https://github.com/aryann6e/Serverless-Emailing-Applications/blob/main/Screenshot%202024-06-28%20233555.png)

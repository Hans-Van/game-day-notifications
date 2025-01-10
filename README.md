# NBA Game Day Notifications / Sports Alerts System

## **Project Overview**
This project focuses on developing a notification system that provides real-time NBA game day score updates to users via SMS or email. By leveraging Amazon SNS, AWS Lambda with Python, Amazon EventBridge, and NBA APIs, it ensures sports enthusiasts receive timely updates. The project serves as a practical example of using cloud computing to build an efficient alert mechanism.

---

## **Key Features**
-Retrieves live NBA game scores using a third-party API.
-Formats and sends game updates to users via SMS or email using Amazon SNS.
-Automates notifications on a schedule through Amazon EventBridge.
-Follows security best practices with IAM policies based on the principle of least privilege.

## **Prerequisites**
-To get started, you’ll need:
-An account at sportsdata.io with an API key for accessing NBA data.
-A personal AWS account with basic knowledge of AWS and Python.

---
## **Technical Architecture**
![nba_API](https://github.com/user-attachments/assets/5e19635e-0685-4c07-9601-330f7d1231f9)

---

## **Technologies Used**
-Cloud Provider: AWS
-Core AWS Services: SNS, Lambda, EventBridge
-External API: NBA Game API from SportsData.io
-Programming Language: Python 3.x
-IAM Security: Roles with least privilege policies for secure access.

---


## **Project Structure**
```bash
game-day-notifications/
├── src/
│   ├── gd_notifications.py          # Main Lambda function code
├── policies/
│   ├── gd_sns_policy.json           # SNS publishing permissions
│   ├── gd_eventbridge_policy.json   # EventBridge to Lambda permissions
│   └── gd_lambda_policy.json        # Lambda execution role permissions
├── .gitignore
└── README.md                        # Project documentation

```

## **Setup Instructions**

## **Clone the Repository**
```bash
git clone https://github.com/ifeanyiro9/game-day-notifications.git
cd game-day-notifications
```

## **Step 1: Create an SNS Topic**
1. Log in to AWS Management Console and navigate to SNS.
2. Create a new topic (Standard type) and name it (e.g., gd_topic).
3. Note the ARN of the topic.

## **Step 2: Add Subscriptions to the Topic**
1. Go to the topic details page and create a new subscription.
2. Choose a protocol:
-Email: Enter a valid email address and confirm the subscription via email.
-SMS: Enter a valid phone number in international format (e.g., +1234567890).
3. For email, confirm the subscription from your inbox.

## **Step 3: Set Up IAM Policies**
In the AWS IAM console, create a policy for SNS access:

1. Go to Policies → Create Policy → JSON tab.
-Paste the content from policies/gd_sns_policy.json.
-Replace placeholders (REGION and ACCOUNT_ID) with your AWS details.
-Save the policy with a name like gd_sns_policy.
2. Repeat the above steps for EventBridge and Lambda policies using the corresponding JSON files.

## **Step 4: Deploy the Lambda Function**
1. Navigate to the AWS Lambda service.
2. Create a new function:
-Choose "Author from Scratch."
-Name the function (e.g., gd_notifications) and set Python 3.x as the runtime.
3. Attach the IAM role created earlier to the function.
4. Add environment variables:
-NBA_API_KEY: Your NBA API key.
-SNS_TOPIC_ARN: The ARN of your SNS topic.
5. Upload or paste the src/gd_notifications.py code into the function editor.
Save and deploy the function.

## **Step 5: Automate with EventBridge**
1. Go to EventBridge and create a new rule.
2. Set the event source to a schedule (e.g., hourly cron jobs).
3. Link the rule to your Lambda function (gd_notifications).

## **Testing the System**
1. Create a test event in Lambda and run the function.
2. Check CloudWatch logs for execution details.
3. Confirm that users receive SMS or email notifications.

## **What I Learnt**
-How to create a notification system using AWS SNS and Lambda.
-Securing services with IAM roles and least privilege policies.
-Automating workflows with EventBridge.
-Integrating external APIs into cloud workflows.

## **Future Enhancements**
-Add support for other sports, like NFL scores.
-Use DynamoDB to store user preferences for personalized alerts.
-Develop a web interface for managing subscriptions and notifications.
  



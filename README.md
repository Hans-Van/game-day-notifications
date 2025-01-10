# NBA Game Day Notifications / Sports Alerts System

## **Project Overview**
This project focuses on developing a notification system that provides real-time NBA game day score updates to users via SMS or email. By leveraging Amazon SNS, AWS Lambda with Python, Amazon EventBridge, and NBA APIs, it ensures sports enthusiasts receive timely updates. The project serves as a practical example of using cloud computing to build an efficient alert mechanism.

## **Key Features**
-Retrieves live NBA game scores using a third-party API.
-Formats and sends game updates to users via SMS or email using Amazon SNS.
-Automates notifications on a schedule through Amazon EventBridge.
-Follows security best practices with IAM policies based on the principle of least privilege.

## **Prerequisites**
-An account at sportsdata.io with an API key for accessing NBA data.
-A personal AWS account with basic knowledge of AWS and Python.

## **Technical Architecture**
![nba_API](https://github.com/user-attachments/assets/5e19635e-0685-4c07-9601-330f7d1231f9)


NBA Game Day Notifications / Sports Alerts System
Project Overview
This project focuses on developing a notification system that provides real-time NBA game day score updates to users via SMS or email. By leveraging Amazon SNS, AWS Lambda with Python, Amazon EventBridge, and NBA APIs, it ensures sports enthusiasts receive timely updates. The project serves as a practical example of using cloud computing to build an efficient alert mechanism.

Key Features
Retrieves live NBA game scores using a third-party API.
Formats and sends game updates to users via SMS or email using Amazon SNS.
Automates notifications on a schedule through Amazon EventBridge.
Follows security best practices with IAM policies based on the principle of least privilege.
Prerequisites
To get started, you’ll need:

An account at sportsdata.io with an API key for accessing NBA data.
A personal AWS account with basic knowledge of AWS and Python.
Technical Architecture
The system integrates various AWS services with external APIs to deliver real-time notifications.

## **Technologies Used**
-Cloud Provider: AWS
-Core AWS Services: SNS, Lambda, EventBridge
-External API: NBA Game API from SportsData.io
-Programming Language: Python 3.x
-IAM Security: Roles with least privilege policies for secure access.

---
## **Project Structure**

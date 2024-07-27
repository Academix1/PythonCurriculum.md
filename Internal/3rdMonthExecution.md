About Project:
User Journey:

1. Sign Up / Log In

   - The user visits the SmartAnalyze website.
   - They create an account using their email or social media credentials (facilitated by AWS Cognito).
   - Returning users simply log in to their existing account.

2. Dashboard

   - After logging in, the user is directed to their personalized dashboard.
   - The dashboard displays an overview of their recent analyses and any saved results.

3. Analyze Text

   - The user clicks on "New Analysis" or a similar button.
   - They're presented with options to either analyze text or upload an image.
   - For text analysis:
     - The user can type or paste the social media post text into a text box.
     - They click "Analyze Text" to submit.
     - The system processes the text using AWS Comprehend.
     - Results are displayed, showing:
       - Overall sentiment (Positive, Negative, Neutral, or Mixed)
       - Sentiment scores (percentage breakdown of sentiments)
       - Identified entities (people, places, organizations mentioned)

4. Analyze Image

   - For image analysis:
     - The user uploads an image of a social media post.
     - They click "Analyze Image" to submit.
     - The system uses AWS Rekognition to:
       - Extract text from the image
       - Perform content moderation
     - The extracted text is then analyzed using AWS Comprehend.
     - Results are displayed, showing:
       - Content moderation results (any flags for inappropriate content)
       - Extracted text
       - Sentiment analysis and entity recognition results for the extracted text

5. View Detailed Results

   - The user can click on any analysis result to view more details.
   - Detailed view might include:
     - Breakdown of sentiment scores
     - List of all identified entities with their types
     - For images: full moderation results and confidence scores

6. Save and Share Results

   - Users can save analyses to their account for future reference.
   - There might be an option to generate a shareable link or export results as a PDF.

7. Historical Analysis

   - Users can access their past analyses from the dashboard.
   - They might be able to compare multiple analyses or track sentiment over time for specific topics or entities.

8. Account Management

   - Users can manage their account settings, update their profile, or change notification preferences.

9. Real-time Updates

   - If the user has multiple analyses running or is part of a team, they might receive real-time updates (via AWS AppSync) when new analyses are completed.

10. Mobile Experience
    - The responsive design allows users to perform all these actions on their mobile devices as well.

Throughout this process, the backend (Django) handles user requests, interacts with AWS services for AI analysis, and manages data storage. The frontend (React) provides a smooth, interactive user interface, updating in real-time as analyses are completed.

This tool would be particularly useful for:

- Social media managers monitoring brand sentiment
- Marketing professionals analyzing campaign impact
- Researchers studying public opinion on various topics
- Business owners keeping track of customer feedback
- Individuals curious about the sentiment and content of their social media posts

The key value proposition of SmartAnalyze is its ability to quickly provide insights into the sentiment and content of social media posts, helping users make data-driven decisions about their social media strategy or research.

#############################################

# SmartAnalyze: AI-Powered Social Media Sentiment Analyzer

## Core Functionality:

- Analyze sentiment in social media posts (text and images)
- Provide entity recognition
- Perform content moderation

## AWS Services Used:

1. EC2: Hosting the Django backend

   - Instance: c5.4xlarge (16 vCPU, 32 GB RAM)
   - Running 6 hours/day, 5 days/week

2. RDS (PostgreSQL): Database for storing user data and analysis results

   - Instance: db.t3.large (2 vCPU, 8 GB RAM)
   - Running 6 hours/day, 5 days/week

3. S3: Store user-uploaded images and static assets

   - Single bucket with folders for each student

4. CloudFront: Content Delivery Network for static assets

5. Cognito: User authentication and management

6. Lambda: Manage start/stop schedule for EC2 and RDS

7. CloudWatch: Monitoring and scheduling

8. Route 53: DNS management (optional)

9. Certificate Manager: SSL/TLS certificates (optional)

## AI Services:

1. Amazon Comprehend:

   - Sentiment analysis
   - Entity recognition

2. Amazon Rekognition:
   - Image analysis
   - Content moderation
   - Text extraction from images

## Infrastructure Sharing Strategy:

1. EC2 Instance:

   - Single EC2 instance hosts all 30 student applications
   - Nginx as reverse proxy to route requests based on subdomains

2. RDS:

   - Single RDS instance with separate schemas for each student

3. S3:

   - Single bucket with folders for each student

4. Cognito:

   - Single user pool with groups for each student application

5. AI Services:
   - Shared endpoints with usage tracked per student

## Terraform Management:

- Daily deployment and teardown of EC2 and RDS instances
- Scheduled using CloudWatch and Lambda

## Student Access:

- Each student gets a subdomain (e.g., student1.smartanalyze.com)
- Isolated database schema and S3 folder
- Cognito group for access control

#################

# SmartAnalyze Cost Breakdown (Terraform-managed)

Assuming 22 working days per month:

1. EC2 Instance:

   - c5.4xlarge: $0.68 per hour
   - 6 hours/day, 22 days/month: $0.68 _ 6 _ 22 = $89.76

2. RDS Instance:

   - db.t3.large: $0.145 per hour
   - 6 hours/day, 22 days/month: $0.145 _ 6 _ 22 = $19.14
   - Storage (100 GB): $0.115 per GB-month \* 100 = $11.50

3. S3:

   - Storage (2 GB per student): 60 GB \* $0.023 per GB-month = $1.38
   - Requests:
     - PUT/COPY/POST/LIST: 50,000 \* $0.005/1,000 = $0.25
     - GET: 500,000 \* $0.0004/1,000 = $0.20

4. CloudFront:

   - Data transfer out (100 GB): 100 \* $0.085 = $8.50
   - Requests (2 million): 2,000,000 \* $0.0075/10,000 = $1.50

5. Cognito:

   - First 50,000 MAUs are free

6. Lambda Function:

   - 44 invocations _ 1000ms _ $0.0000166667 per 100ms = $0.00073 (negligible)

7. CloudWatch:

   - Two rules: $1.00 per rule per month \* 2 = $2.00
   - Logs (5 GB): 5 \* $0.50 = $2.50

8. Route 53 (optional):

   - Hosted zone: $0.50 per month
   - Queries (1 million): $0.40

9. Certificate Manager:

   - Free for public SSL/TLS certificates

10. Comprehend:

    - Assuming 100,000 units of text per month: 100,000 \* $0.0001 = $10.00

11. Rekognition:

    - Assuming 10,000 images per month: 10,000 \* $0.001 = $10.00

12. Data Transfer:
    - Assuming 100 GB out to internet: 100 \* $0.09 = $9.00

Total Estimated Monthly Cost: $166.63

Cost per student per month: $166.63 / 30 = $5.55

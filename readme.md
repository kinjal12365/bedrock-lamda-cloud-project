# AWS Lambda Blog Generator using Amazon Bedrock and saving in s3 bucket

## 📌 Overview
This project uses Amazon Bedrock's Meta LLaMA3-70B model to generate a 200-word blog on a given topic and stores the output in an S3 bucket. The application is designed to run within an AWS Lambda function.

---

## 🧱 Components
- **AWS Lambda**: Executes the Python function when triggered.
- **Amazon Bedrock**: Generates the blog using a foundation model.
- **Amazon S3**: Stores the generated blog as a `.txt` file.

---

## 🚀 Features
- Accepts blog topic dynamically via API input.
- Generates realistic and relevant blog content using LLaMA3.
- Saves the output in an organized folder structure (`blog-output/HHMMSS.txt`) inside an S3 bucket.

---

## 📥 Input
The Lambda function expects a JSON input in the following format:

```json
{
  "body": "{\"blog_topic\": \"Climate Change and Future\"}"
}

📤 Output
Blog content is saved in the S3 bucket named bedrocklambdatutorial.

Filename format: blog-output/HHMMSS.txt (based on current time).

⚙️ Configuration
Make sure to:

Give your Lambda function permissions to invoke bedrock:InvokeModel and write to your S3 bucket and you can give full acess.

Ensure the region is set to us-east-1 (or update it as needed).

Update the S3 bucket name if you're using a different bucket.

And also set the api gateway properly

Additional boto3 latest version installation is also needed to locally download it convert it into a zip file and add it as a layer.

Finally use postman to post the requests.
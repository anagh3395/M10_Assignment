# M10 Assignment 
This project demonstrates how to scrape data from a website using Selenium WebDriver, store it in a pandas DataFrame, and upload it to a publicly accessible Amazon S3 bucket using the Boto3 library.

### Dependencies

Selenium (pip install selenium)
Boto3 (pip install boto3)
WebDriver Manager (pip install webdriver-manager)

### AWS Configuration

Set Up AWS Credentials:

- Create an IAM user with programmatic access and download the credentials as a JSON file.
- Configure your AWS environment variables (AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY) to point to these credentials. You can do this permanently in your system's environment variables or temporarily within your Python script.

Create a Public S3 Bucket:

 Use the AWS Management Console or AWS CLI to create an S3 bucket.
- Make sure the bucket policy allows public read access for the objects you plan to upload. Here's an example bucket policy for public read access:

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": {
                "AWS": "*"
            },
            "Action": [
                "s3:GetObject"
            ],
            "Resource": [
                "arn:aws:s3:::<your-bucket-name>/*"
            ]
        }
    ]
}


### Part 1

Step 1. Load the script, M10_webscraper_assignment.ipybn into your repository
Step 2. Create an s3 bucket to store your outputs of csv files.. Be sure to make the settings on the s3 buckets public. As part of configuration of the awscli, you should ensure that you have access to s3 and the AWS environment. Note see below in the code snipper where you will have to enter the name of your s3 bucketL
 
Step 3. Update the M10_webscraper_assignment.ipybn file to include your s3 path
Step 4. Test the file by inspecting the output on the s3 bucket
Step 5. Once the test has passed, commit the changes to the master branch of your GitHub repository
Step 6. Note that the output of the file has an issue! The header inserts a blank row!

![image](https://github.com/anagh3395/M10_Assignment/assets/146588429/6af9d049-4630-4637-a152-0ad13a7e0dfa)

![image](https://github.com/anagh3395/M10_Assignment/assets/146588429/e61bcdde-6c6d-4a57-b93b-9bb4cc04602b)


Update the script that was provided to remove the blank row in the csv output file

![image](https://github.com/anagh3395/M10_Assignment/assets/146588429/a8e75d35-c140-48ae-bca4-2dad9a0df3f8)

![image](https://github.com/anagh3395/M10_Assignment/assets/146588429/e79542de-ade3-4b67-b2d3-79adcb916b60)



Step 7. Test the file by inspecting the output on the s3 bucket
Step 8. Once the test has passed, commit the changes to your script the master branch of your GitHub repository
Step 9. Provide evidence that the file and script were successfully updated by providing the link to s3 and the .ipybn file in the repository. 

### Part 2
For this portion of the lab, we are going to alter the script, M10_webscraper_assignment.ipybn, to iterate through the pagination that exists on the page and compile all of the results in one dataframe from each page.

![image](https://github.com/anagh3395/M10_Assignment/assets/146588429/11598451-9e4b-489c-ba37-cfa1b8251b89)

![image](https://github.com/anagh3395/M10_Assignment/assets/146588429/f7c33469-169c-4184-bae4-1c25d33716b4)


Once the test has passed, commit the changes to the master branch of your GitHub repository, updating the script and the file on s3.  






**Google Analytics Data Export to BigQuery**
This Python script extracts data from Google Analytics and loads it into Google BigQuery. Big thanks to gpt4 for helping with the documentation <3

Table of Contents
Pre-requisites
Setup Instructions
Running the Script
Pre-requisites

To use this script, you will need:

Python 3.7 or higher installed on your machine. You can download Python from the official website here
A Google Cloud account with a project where you have permissions to create and manage BigQuery datasets and tables.
Access to a Google Analytics account and view, with a service account that has permissions to read data from this view.
A service account key file (in JSON format) for authenticating your requests to the Google Analytics API and Google BigQuery.
The google-api-python-client, google-auth, google-cloud-bigquery, and google-auth-httplib2 Python libraries installed in your Python environment.
Setup Instructions
Follow these steps to set up your environment:

Install the Required Python Libraries
Run the following command in your terminal to install the necessary Python libraries:

pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib google-auth google-cloud-bigquery
Set Up Your Google Cloud and Google Analytics Access
In the Google Cloud Console, create a new project (or select an existing one).
Enable the Google Analytics API and BigQuery API for your project.
Create a service account for your project in the IAM & Admin section, and generate a JSON key file for this account.
In the IAM section, give your service account the roles of "BigQuery Data Editor" and "BigQuery Job User" (for BigQuery access), and "Viewer" role (for Google Analytics access).
In your Google Analytics account, add the service account email as a user with Read & Analyze permissions at the view level.
Set Up Your Python Script
Download the Python script.
Replace the placeholder values in the script with your actual values:
Replace 'temp.json' with the path to your service account key file.
Replace 'VIEW ID HERE' with your Google Analytics view ID.
Replace 'INSERT PROJECT ID' with your Google Cloud project ID.
Replace 'INSERT DATASET ID' with your BigQuery dataset ID.
Edit the report_requests list to include the Google Analytics reports you want to export, specifying the metrics and dimensions for each report.
Running the Script
To run the script, navigate to the directory containing the script in your terminal and run the command:

python your_script_name.py
Replace 'script.py' with the actual name of the Python script.

SEO so this can find the right people

Moving Google Analytics to BigQuery. Move GA3 to BigQuery. Transfer GA3 to BigQuery. Migrate Google Analytics Data to BigQuery. Migrate Google Analytics Data into to BigQuery.

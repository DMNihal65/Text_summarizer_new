# Text Summarizer using Pegasus Transformer Model
This project is an implementation of a text summarizer using the Pegasus transformer model, along with AWS CI/CD deployment using GitHub Actions. The text summarizer is capable of taking in a piece of text and generating a concise summary of its content.
## Table of Contents
Installation
Usage
Deployment with AWS CI/CD
Contributing
License

## Installation
To set up the text summarizer on your local machine, follow these steps:
Clone the repository to your local machine:
''shell 
git clone https://github.com/your-username/text-summarizer.git

## Navigate to the project directory:
''shell 
cd text-summarizer

Install the required dependencies. It is recommended to use a virtual environment:
# Create a virtual environment (optional but recommended)
python3 -m venv venv
source venv/bin/activate

# Install the dependencies
pip install -r requirements.txt

Download the Pegasus transformer model. You can use the Hugging Face library to download the model:
python -c "from transformers import PegasusTokenizer, PegasusForConditionalGeneration; PegasusTokenizer.from_pretrained('google/pegasus-xsum'); PegasusForConditionalGeneration.from_pretrained('google/pegasus-xsum')"

This will download the Pegasus tokenizer and the pre-trained model.
Usage
Once you have installed the project and the dependencies, you can use the text summarizer by following these steps:
Import the summarizer module into your Python script:
from summarizer import Summarizer

Create an instance of the Summarizer class:
summarizer = Summarizer()

Provide the text you want to summarize as input:
text = "This is the input text you want to summarize."

Generate the summary:
summary = summarizer.summarize(text)

The summary variable will contain the generated summary.
You can also specify the maximum length of the summary by passing the max_length parameter to the summarize() method. For example:
summary = summarizer.summarize(text, max_length=100)

This will limit the summary to a maximum of 100 tokens.
Deployment with AWS CI/CD
This project utilizes AWS CI/CD for automated deployment using GitHub Actions. The CI/CD pipeline is configured to trigger a deployment on every push to the main branch.
To set up the AWS CI/CD deployment, follow these steps:
Set up an AWS account if you don't have one already.
Create an AWS IAM user with the necessary permissions for the deployment. Note down the Access Key ID and Secret Access Key.
Open the project in your GitHub repository.
Go to the repository's Settings and navigate to the Secrets tab.
Add the following secrets:
AWS_ACCESS_KEY_ID: The Access Key ID of your IAM user.
AWS_SECRET_ACCESS_KEY: The Secret Access Key of your IAM user.
Save the secrets.
Now, whenever you push changes to the main branch, GitHub Actions will automatically trigger the CI/CD pipeline, deploying the updated version of the text summarizer to your AWS infrastructure.
Contributing
Contributions to this project are welcome! If you would like to contribute, please follow these steps:
Fork the repository.
Create a new branch for your feature or bug fix:
git checkout -b feature/your-feature-name

Make your changes and commit them.
Push your changes to your forked repository.
Create a new pull request from your forked repository to the original repository.
Once your pull request is submitted, it will be reviewed by the project maintainers. Thank you for your contribution!
License
This project is licensed under the MIT License.

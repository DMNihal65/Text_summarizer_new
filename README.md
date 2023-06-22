# Text Summarizer using Pegasus Transformer Model

This project is an implementation of a text summarizer using the Pegasus transformer model, along with AWS CI/CD deployment using GitHub Actions. The text summarizer is capable of taking in a piece of text and generating a concise summary of its content.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Deployment with AWS CI/CD](#deployment-with-aws-cicd)
- [Contributing](#contributing)
- [License](#license)

## Installation

To set up the text summarizer on your local machine, follow these steps:

1. Clone the repository to your local machine:

   ```shell
   git clone https://github.com/your-username/text-summarizer.git
2. Navigate to the project directory:

   ```shell
   cd text-summarizer

   
3. Install the required dependencies. It is recommended to use a virtual environment:
  
  ```shell
   # Create a virtual environment (optional but recommended)
python3 -m venv venv
source venv/bin/activate

# Install the dependencies
pip install -r requirements.txt

4.Download the Pegasus transformer model. You can use the Hugging Face library to download the model:
```shell
   python -c "from transformers import PegasusTokenizer, PegasusForConditionalGeneration; PegasusTokenizer.from_pretrained('google/pegasus-xsum'); PegasusForConditionalGeneration.from_pretrained('google/pegasus-xsum')"


# Deployment with AWS CI/CD
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
Now, whenever you push changes to the main branch, GitHub Actions will automatically

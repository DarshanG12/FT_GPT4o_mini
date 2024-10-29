#  Fine-Tuning Project

## Introduction

The **Organization Fine-Tuning Project** aims to utilize OpenAI's language models to create a customized AI assistant that can accurately provide information about both employees and the organization as a whole. By fine-tuning the model with specific data related to the organization and its workforce, we intend to enhance its ability to answer queries regarding organizational structure, employee roles, responsibilities, and other pertinent details.

This project serves as a demonstration of the process for preparing training data, fine-tuning a model, and utilizing the fine-tuned model to respond effectively to questions about the organization and its employees.

## Features

- Fine-tuned OpenAI model to answer questions about employee roles, responsibilities, and organizational details.
- Structured data format using JSON Lines for efficient training data handling.
- Seamless integration with the OpenAI API for querying the model.

## Requirements

- Python 3.11+
- OpenAI Python library
- `jsonlines` library

## Installation

1. **Clone the Repository:**
   ```bash
   https://github.com/DarshanG12/FT_GPT4o_mini.git
   
## 2) Install Required Packages:
```bash
pip install openai jsonlines
```

3) Set Your OpenAI API Key:
Make sure to set your OpenAI API key as an environment variable:
```
export OPENAI_API_KEY='your-api-key'
```

4)Data Preparation
The training data is formatted in JSON Lines, allowing for efficient processing of large datasets. Each entry in the dataset simulates a conversation, providing context about employees and the organization.

Example Data Format:
```
{
    "messages": [
        {"role": "system", "content": "You are an expert on organizational information."},
        {"role": "user", "content": "What is the structure of the organization?"},
        {"role": "assistant", "content": "The organization has three main departments: Sales, Marketing, and Development."}
   ]
}
```
Save your data in a file named YOUR_FILENAME.jsonl.

Run the Fine-Tuning Script: upload the training data and initiate the fine-tuning process:
Monitor Fine-Tuning Status: The script will provide feedback on the status of the fine-tuning job.

Cleanup
To remove the fine-tuned model when it is no longer needed, use the following command:
openai.Model.delete('your-fine-tuned-model-id')










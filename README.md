# Retail Reviews Classifier with Hugging Face Llama on SageMaker  

This repository contains a Jupyter Notebook (`retail_reviews_classification.ipynb`) designed to classify customer reviews for a retail company. The solution leverages the powerful **Hugging Face Llama 3.1 70B Instruct** model, integrated with **Amazon SageMaker**, for high-performance large language model (LLM) inference.  

## Features  
- Classify customer reviews based on predefined labels.  
- Integration with Hugging Face and SageMaker.  
- Outputs a processed CSV containing analysis results for further use.  

---

## Prerequisites  

Before running this project, ensure the following:  

1. **Hugging Face Setup:**  
   - Create a Hugging Face account.  
   - Obtain an API token.  
   - Request access to the **Llama 3.1 70B Instruct model** [here](https://huggingface.co/meta-llama/Llama-3.1-70B-Instruct).  

2. **AWS SageMaker Setup:**  
   - Ensure you have an AWS account with access to SageMaker Studio.  
   - Request access to the `ml.g6.48xlarge` instance type.

3. **Input Data:**  
   - Prepare a CSV file containing customer reviews.  
   - The file must include the following fields:  
     - `Comment` (the review text).  
     - `Score` (numerical rating).  
   - Additional fields are optional but won’t impact the script’s functionality.  

---

## Instructions  

1. **SageMaker Studio Preparation:**  
   - Log into SageMaker Studio.  
   - Upload the following files to your SageMaker environment:  
     - `retail_reviews_classification.ipynb` (this notebook).  
     - Your reviews CSV file.  

2. **Environment Setup:**  
   - Open the notebook in SageMaker Studio.  
   - Install required dependencies by running the `pip install` commands at the top of the notebook.  

3. **Model Inference:**  
   - Run the notebook's step-by-step code to classify reviews.  
   - The script will generate a processed CSV file with classification results in your file system (visible in the left panel of SageMaker Studio).  

4. **Download Processed Results:**  
   - Download the generated CSV to your local machine for further use or analysis.  

5. **Cost Management (VERY IMPORTANT):**  
   - At the end of your session, **run the cleanup code** provided in the notebook to delete the deployed model and endpoint.  
   - **Stop the running kernel**.  See the commented instructions at the bottom of the ipynb file.
   - These steps are crucial to control AWS costs!!

---

## License  

This project is licensed under the [MIT License](LICENSE).  


# Retail Reviews Classification with Llama 3.1 70B on SageMaker

This repository contains a SageMaker-compatible Jupyter Notebook (`ipynb`) for classifying retail customer reviews using the Hugging Face integration with the **Llama 3.1 70B model**. This script is designed to be user-friendly for anyone familiar with SageMaker Studio. It performs sentiment classification based on `Comment` and `Score` fields in a reviews dataset and outputs a processed CSV file.

---

## **Quick Start Guide**

### Prerequisites

Before running the code, ensure you have:
- Access to **Amazon SageMaker Studio**.
- Permissions for **ml.g6.48xlarge** instance type (or similar high-performance instances).
- A `.csv` file containing customer reviews with the fields:
  - **`Comment`** (required): The review text.
  - **`Score`** (required): Numeric rating associated with the review.

Other fields in the CSV are ignored by this script but can be present.

---

### **Steps to Use**

1. **Set Up Your SageMaker Environment**
   - Ensure you have an AWS account with permissions to create SageMaker resources.
   - Create or select a **domain** and **user profile** within SageMaker.

2. **Launch SageMaker Studio**
   - Log into SageMaker Studio from your AWS Management Console.

3. **Upload Necessary Files**
   - Upload the `.ipynb` file from this repository into SageMaker Studio.
   - Upload your reviews dataset CSV (with `Comment` and `Score` fields) into SageMaker Studio.

4. **Install Required Libraries**
   - Use the `pip install` commands provided at the top of the notebook to set up the required environment.

5. **Run the Notebook**
   - Execute the cells in sequence:
     - The notebook will load your dataset, classify the reviews using the Llama 3.1 model, and save the processed results as a new CSV file.
     - The output CSV will be available in the file system panel to the left of your SageMaker Studio interface.

6. **Download the Processed CSV**
   - Locate the output file in the SageMaker file browser.
   - Download it to your local machine for further analysis.

7. **Clean Up Resources**
   - **Run the cleanup code at the bottom of the notebook!**
     - This will delete the deployed model and endpoint to prevent unnecessary charges.
   - **Terminate the SageMaker kernel**:
     - Follow the instructions in the code comments to stop the running kernel.

---

### **Important Notes on Cost Management**

- The `ml.g6.48xlarge` instance type is resource-intensive. Be mindful of your runtime.
- Ensure you **delete the endpoint and model** after running the notebook. The cleanup steps are provided in the notebook and must be executed to avoid incurring extra costs.
- Double-check that the kernel is stopped when you're done.

---

### Example Output

The processed CSV will contain:
- The original fields (`Comment`, `Score`, etc.).
- Additional classification results, such as sentiment labels.

---

### **Troubleshooting**

If you encounter any issues:
- Check your AWS permissions for SageMaker resource creation.
- Ensure your CSV file has the required fields (`Comment` and `Score`).
- Review the error messages in the SageMaker Studio logs for more details.

---

### **License**

This project is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute this code.



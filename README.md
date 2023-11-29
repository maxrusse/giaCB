# giaCB (Gastrointestinal Imaging-Aware Chatbot)

## Overview

giaCB is a context-aware GPT-4 based chatbot designed to provide differential diagnoses in gastrointestinal radiology, aiming to enhance AI-assisted diagnostic tools in the field.

### Highlights

  - Demonstrates high performance in gastrointestinal differential diagnosis.
  - Outperforms generic GPT-4 models in providing contextual responses and diagnostic support.
  - **Potential Impact**: Could significantly improve the efficiency and accuracy of diagnostic processes in radiology.

### Important Note

  - **Status of Research**: This project is part of an ongoing research initiative and the details of the study may change pending peer review.
  - **Caution for Use**: The tool is not intended for medical use and should be used accordingly.

## Flask Application for Query Processing

This Flask application is designed to process queries using a GPT-4 based model, extracting relevant information from a specified document directory and serving it through a web interface.

### Prerequisites

Before you begin, ensure you have met the following requirements:

  - Python 3.x installed on your system.
  - Flask and other dependencies installed (use `pip install -r requirements.txt`).
  - An OpenAI API key.

### Installation and Setup

1. **Clone the Repository:**
  - Use the following command to clone the giaCB repository:
  ```
  git clone https://github.com/maxrusse/giaCB
  ```
  - Then, change to the repository directory:
  ```
  cd giaCB
  ```

2. **Install Dependencies:**
  - Install the required Python packages using:
  ```
  pip install -r requirements.txt
  ```

3. **Set OpenAI API Key:**
  - You can set the API key as an environment variable:
  ```
  export OPENAI_API_KEY='your-api-key'
  ```
  - Alternatively, the application will prompt you to input the API key when it's run.

### Running the Index Creation

1. **Prepare Your Environment:**
  - Ensure you have set the `OPENAI_API_KEY` as an environment variable. This is crucial for the script to access OpenAI's GPT models.
  - If the environment variable is not set, the script will prompt for the API key when run.

2. **Specify Folder Paths:**
  - The script requires two command-line arguments:
  - `pdf_folder`: The path to the folder containing the PDF documents.
  - `index_folder`: The path to the folder where the indexed data will be saved.

3. **Run the Script:**
  - Execute the index creation script using the following command:
  ```
  python gia_data_processing.py [path_to_pdf_folder] [path_to_index_folder]
  ```
  - Replace `[path_to_pdf_folder]` and `[path_to_index_folder]` with the respective folder paths.

4. **Verification:**
  - After successful execution, the script will process the documents in the specified PDF folder and save the indexed data in the index folder.
  - A confirmation message will be displayed: "Documents processed and saved to [index_folder]."

## Running the Application

1. **Start the Flask Server:**
  - Run the Flask application using the following command:
  ```
  python gia_app.py [index_folder]
  ```
  - Optionally, specify the index folder path as a command-line argument. If not provided, the application will prompt for it.

2. **Accessing the Application:**
  - Navigate to `http://localhost:8000` (or the appropriate port) in your web browser.


3. **Using the Application:**
  - Enter a query in the provided text box and submit.
  - The application will process the query and display the results, including relevant document references.

## License

This project is licensed under the MIT Licence. See the LICENSE file for more details.
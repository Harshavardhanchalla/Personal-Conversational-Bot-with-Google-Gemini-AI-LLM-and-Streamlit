# Harsha's-Personal-Conversational-Bot-with-Google-Gemini-AI-LLM-and-Streamlit

### Project Title
**Conversational Bot with Google Gemini AI LLM and Streamlit**

### README.md

```markdown
# Conversational Bot with Google Gemini AI LLM and Streamlit

This project leverages the Google Gemini AI LLM to create an interactive conversational bot using Streamlit. The bot uses the Generative AI model from Google to provide intelligent responses based on user input. The application is deployed on a Streamlit interface, providing a seamless and interactive user experience.

## Table of Contents
- [Project Description](#project-description)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Credits](#credits)
- [License](#license)

## Project Description
The Conversational Bot is designed to engage users in natural language conversations. It utilizes Google's Gemini AI LLM, a powerful language model capable of understanding and generating human-like text. This project demonstrates the integration of the Gemini AI model with a user-friendly Streamlit interface, allowing users to interact with the model in real-time.

## Features
- **Interactive Interface**: Simple and intuitive user interface built with Streamlit.
- **Real-time Responses**: Get instant responses from the Google Gemini AI model.
- **Streamlined Setup**: Easy to configure and deploy on local or cloud environments.
- **Expandable**: The project can be easily expanded to include more complex interactions and functionalities.

## Installation
Follow these steps to set up the project on your local machine:

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/conversational-bot-gemini.git
    cd conversational-bot-gemini
    ```

2. **Create and activate a virtual environment** (optional but recommended):
    ```sh
    python -m venv env
    source env/bin/activate   # On Windows use `env\Scripts\activate`
    ```

3. **Install the required libraries**:
    ```sh
    pip install -r requirements.txt
    ```

4. **Set your Google Gemini API key**:
    - Create a `.env` file in the project directory and add your API key:
    ```sh
    GEMINI_API_KEY=your_api_key_here
    ```

## Usage
1. **Run the Streamlit app**:
    ```sh
    streamlit run app.py
    ```

2. **Interact with the bot**:
    - Open your web browser and go to `http://localhost:8501`.
    - Enter your question in the input field and click "Answer to your question".
    - The bot will provide a response using the Google Gemini AI model.

## Code Explanation
### Import Libraries and Configure API Key
```python
import streamlit as st
import os
import pathlib
import textwrap
from IPython.display import display, Markdown

# Configure API key for Google Gemini
os.environ['GEMINI_API_KEY'] = ''
import google.generativeai as genai
genai.configure(api_key=os.environ['GEMINI_API_KEY'])
```

### Function to Load Google Gemini Model and Get Responses
```python
model = genai.GenerativeModel('gemini-pro')
chat = model.start_chat(history=[])
def get_gemini_response(question):
    response = chat.send_message(question, stream=True)
    return response
```

### Initialize Streamlit App
```python
st.set_page_config(page_title="Conversational Bot")

st.header("Harsha's Personal Gemini AI LLM ")

input = st.text_input("Input: ", key="input")

submit = st.button("Answer to your question")

if submit:
    response = get_gemini_response(input)
    st.subheader("The Response is")
    for chunk in response:
        st.write(chunk.text)
        st.write("_" * 80)
    
    st.write(chat.history)
```

## Credits
- **Author**: Harsha
- **Mentor**: KODI PRAKASH SENAPATI
- **Libraries**:
  - Streamlit
  - OpenAI
  - pathlib
  - textwrap

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

### Additional Notes:
- Make sure to replace `Challa harsha Vradhan` with your actual GitHub username in the clone URL.
- Ensure your `.env` file is correctly configured with your actual Google Gemini API key.
- You can customize and extend the project to include additional features such as user authentication, more advanced NLP processing, or integration with other APIs.

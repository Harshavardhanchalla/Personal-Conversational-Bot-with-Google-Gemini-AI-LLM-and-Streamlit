# Harsha's-Personal-Conversational-Bot-with-Google-Gemini-AI-LLM-and-Streamlit

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
### Usage

1. **Run the Streamlit app**:
   - Open a terminal or command prompt.
   - Navigate to the directory where the project is located.

2. **Install Required Libraries**:
   - Ensure you have Python installed on your machine.
   - Install the necessary libraries listed in the `requirements.txt` file using pip. This includes libraries such as `streamlit`, `google.generativeai`, and others required for the project.

3. **Set Up Google Gemini API Key**:
   - Obtain your Google Gemini API key.
   - Set the API key as an environment variable. You can do this by creating a `.env` file in the project directory and adding your API key there.

4. **Run the Application**:
   - In the terminal, run the Streamlit app using the `streamlit run` command followed by the name of the Python file (`app.py` in this case).
   - Streamlit will start a local server and provide a URL (usually `http://localhost:8501`).

5. **Interact with the Bot**:
   - Open your web browser and go to the provided URL.
   - You will see a user interface where you can input your questions.
   - Enter your question in the input field and click the button to get a response from the bot.
   - The bot will process your question using the Google Gemini AI model and display the response in real-time.

By following these steps, you can easily set up and run the conversational bot on your local machine, leveraging the power of Google Gemini AI for intelligent interactions.
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

### Additional Notes:
- Make sure to replace `Challa harsha Vradhan` with your actual GitHub username in the clone URL.
- Ensure your `.env` file is correctly configured with your actual Google Gemini API key.
- You can customize and extend the project to include additional features such as user authentication, more advanced NLP processing, or integration with other APIs.

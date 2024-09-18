#NLP Emotion Detection with IBM Watson

#Table of Contents:
Project Overview
Features
Technologies Used
Installation
Usage
Project Structure
Error Handling
Testing
Contributing
License
Acknowledgments

#Project Overview:
This project implements an emotion detection application using IBM Watson's Natural Language Understanding (NLU) API. The app takes a user-inputted text and analyzes it to predict the emotional tone behind the text, such as anger, disgust, fear, joy, or sadness. It utilizes IBM's powerful Watson AI service for natural language processing and sentiment analysis.

This project aims to demonstrate how to integrate a cloud-based AI model into a Flask-based web application, providing a clean and intuitive interface for users.

#Features:
1. Emotion Analysis: Analyze text for various emotions, including anger, disgust, fear, joy, and sadness.
2. Dominant Emotion Detection: Identifies the most prominent emotion in a given piece of text.
3. Error Handling: Gracefully handles errors like blank input, network failures, and API timeouts.
4. Web Interface: A user-friendly web interface built using HTML, CSS, and JavaScript for seamless interaction.
5. Real-time Feedback: Provides immediate emotion detection results to the user.

#Technologies Used:
1. Python 3.7+: Main programming language.
2. Flask: Python micro-framework for building web applications.
3. IBM Watson NLU API: Cloud-based natural language understanding API for emotion detection.
4. Requests: Python library used to send HTTP requests to Watson's API.
5. HTML5, CSS3, JavaScript: For the web interface and user interaction.
6. Bootstrap: Front-end framework for styling the web interface.

#Installation:
Prerequisites:
1. Python 3.7+ must be installed on your local machine.
2. A free IBM Cloud account to access IBM Watson API.

#Step-by-Step Installation:
1. Clone the Repository:
git clone https://github.com/your-username/emotion-detection-watson.git
cd emotion-detection-watson

2. Create a Virtual Environment:
python3 -m venv .venv
source .venv/bin/activate

3. Install Required Packages Install dependencies listed in requirements.txt:
pip install -r requirements.txt

4. Set Up IBM Watson NLU API:
  A. Go to the IBM Cloud and create an instance of Natural Language Understanding.
  B. Get your API key and URL from the service credentials.

5. Update these credentials in your Python code:
authenticator = IAMAuthenticator('YOUR_API_KEY')
nlu.set_service_url('YOUR_API_URL')

6. Run the Flask Application:
python server.py

7. Access the App Open your browser and navigate to:
http://127.0.0.1:5000

#Usage:
1. Open the app in your browser.
2. Enter any text you would like to analyze for emotions.
3. Press the Run Sentiment Analysis button.
4. The app will display the predicted emotions along with the dominant emotion.

#Project Structure:
emotion-detection-watson/
│
├── EmotionDetection/         # Module for Watson API integration
│   ├── __init__.py
│   ├── emotion_detection.py  # Contains the emotion_detector function
│
├── static/                   # Frontend JavaScript, CSS files
│   ├── mywebscript.js
│
├── templates/                # HTML templates for Flask rendering
│   └── index.html
│
├── server.py                 # Main Flask application
├── requirements.txt          # List of Python dependencies
└── README.md                 # Project documentation

#Error Handling
1. Blank Input: If no text is entered, the system will display a message saying, "Invalid text! Please try again."
2. API Request Timeout: If the request to the Watson API times out, the application will handle it gracefully and return an error message to the user.
3. Unexpected API Response: If the API returns a non-200 response, the application will treat it as an error and return None for all emotions.
4. All error handling is centralized in the emotion_detector function.

#Testing

#To test the application:
1. Run the following command:
python test_emotion_detection.py

2. Check the terminal for test results.
3. The following test cases are covered:
  A. Blank input test
  B. Valid input test
  C. Error handling for invalid API responses

#Contributing
Contributions are welcome! If you'd like to contribute, please fork the repository and submit a pull request.

#Steps to contribute:
1. Fork the repo
2. Create a new branch (git checkout -b feature-branch)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin feature-branch)
5. Create a new Pull Request

#License
This project is licensed under the MIT License - see the LICENSE file for details.

#Acknowledgments
1. IBM Watson: For providing the Natural Language Understanding API.
2. Flask Documentation: For the excellent documentation on building web apps.
3. Bootstrap: For styling the web interface.

ASL to Text Translation Interface

This project is a Flask-based web application for translating American Sign Language (ASL) gestures into text using a pretrained deep learning model. The system leverages EfficientNet for gesture recognition and provides an intuitive web interface for users to upload ASL gesture images and receive text translations.

Key Features

ASL Gesture Recognition: Supports translation of 29 ASL classes, including letters (A-Z), and special tokens (del, space, nothing).
Pretrained Model: Uses an EfficientNet model trained on ASL gesture data to deliver accurate predictions.

Web Interface: A user-friendly frontend built with HTML, CSS, and JavaScript for uploading images and displaying results.
Real-Time Predictions: Dynamically translates uploaded ASL gesture images into text.

Project Workflow

Frontend: Users upload ASL gesture images via a web interface.
Backend: The Flask server processes the images, runs them through the pretrained model, and predicts the corresponding ASL gesture.
Output: The predicted text is returned to the frontend and displayed to the user.

Technologies Used

Backend
Flask: Serves the application and handles API routes for prediction.
PyTorch: Loads and executes the EfficientNet-based pretrained model.
Frontend
HTML, CSS, JavaScript: Implements an intuitive web interface for uploading images and viewing predictions.

Model

EfficientNet: A pretrained deep learning model with a modified output layer to support 29 ASL classes.

Setup and Execution

Ensure Python (3.8 or later) and required dependencies are installed.
Place the pretrained model file (efficientnet_model.pth) in the specified path.

Run the application:

bash
Copy code
python app.py  
Access the interface via http://127.0.0.1:5000/ in a web browser.

Input Details

Accepted Input: Images of ASL gestures in .jpg, .png, or similar formats.
Image Preprocessing: The system resizes the image to 128x128 pixels and converts it into a tensor before prediction.

Output Details

Prediction: The application returns the corresponding ASL character or special token (space, del, nothing).
Response: The response includes the predicted class label and its corresponding index.

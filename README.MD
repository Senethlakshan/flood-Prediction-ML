# Flask App for Flood Prediction

## Overview

This Flask application is designed to predict flood probabilities using a pre-trained deep learning model. The application leverages various Python libraries for data manipulation, visualization, and machine learning. The model is based on a neural network that was trained on flood prediction data to provide accurate flood probability forecasts.

## Project Structure

- **`app.py`**: Main Flask application file.
- **`model.pkl`**: Serialized deep learning model for flood prediction.
- **`data/`**: Directory containing datasets (e.g., `train.csv`, `test.csv`).
- **`requirements.txt`**: List of dependencies required to run the application.
- **`README.md`**: This file.

## Setup

### Prerequisites

Ensure you have the following installed:

- Python 3.8 or higher
- pip (Python package installer)

### Install Dependencies

1. Clone the repository:

    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. Install the required packages:

    ```bash
    pip install -r requirements.txt
    ```

### Requirements File

Create a `requirements.txt` file with the following content:

```plaintext
Flask==2.0.1
pandas==1.3.2
matplotlib==3.4.3
seaborn==0.11.2
scipy==1.7.1
numpy==1.21.2
scikit-learn==0.24.2
tensorflow==2.6.0

--------------------------------------------------------------------------------++

Usage
Running the Application
Navigate to the directory containing app.py.

Run the Flask application:

bash
Copy code
python app.py
The Flask app will start running on http://127.0.0.1:5000/. You can access it via your web browser or use tools like curl or Postman to interact with the API endpoints.

API Endpoints
/predict: Endpoint for making predictions.
Method: POST
Request Body: JSON object containing features for prediction.
Response: JSON object with the predicted flood probability.
Model Details
Model Training
The model was trained using a neural network with the following architecture:

Input layer with 256 neurons and ReLU activation
Hidden layers with 128, 64, 32, and 16 neurons, respectively, all using ReLU activation
Output layer with a single neuron for regression
The model was compiled using Mean Squared Error (MSE) loss and the Adam optimizer. The model's performance was evaluated based on the R-squared score.
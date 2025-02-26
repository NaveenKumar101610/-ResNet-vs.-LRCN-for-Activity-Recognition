# Action Recognition Video Splitter

A Streamlit web application that analyzes videos and segments them based on detected actions using deep learning models.

## Overview

This application uses deep learning models (ResNet and CNN-LSTM) to:
- Analyze uploaded videos
- Detect 30 different types of actions
- Split videos into segments based on action transitions
- Display timestamps for each detected action

## Getting Started

### Prerequisites

- Python 3.7 or higher
- pip package manager

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/action-recognition-splitter.git
cd action-recognition-splitter
```

2. Create and activate virtual environment (recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

3. Install required packages
```bash
pip install -r requirements.txt
```

### Required Model Files
Download and place these model files in your project directory:
- `activity_recognition.h5` (ResNet model)
- `activity_recognition2.h5` (CNN-LSTM model)

## Usage

1. Start the application:
```bash
streamlit run app.py
```

2. Open your browser and go to http://localhost:8501

3. Upload an MP4 video

4. Select either ResNet or CNN-LSTM model

5. View the segmented results showing:
   - Segment number
   - Start frame
   - End frame
   - Detected action

## Supported Actions

The system can recognize 30 different actions including:
- ApplyEyeMakeup
- ApplyLipstick
- Archery
- BabyCrawling
- BalanceBeam
- BandMarching
- BaseballPitch
- Basketball
- BasketballDunk
- BenchPress
- And more...

## Project Structure
```
action-recognition-splitter/
│
├── app.py              # Main Streamlit application
├── utils.py           # Video processing utilities
├── requirements.txt   # Project dependencies
├── classes.txt        # Action class labels
└── README.md         # Project documentation
```

## Technical Specifications

- Frame Size: 64x64 pixels
- Frame Sequence Length: 15 frames
- Input Format: MP4 video
- Model Input Shape: (1, 15, 64, 64, 3)
- Output: 30 action classes

## Dependencies
```
numpy
opencv_python
pandas
streamlit
keras==2.12.0
tensorflow==2.12.0
```


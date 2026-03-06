🚁 UAV Indoor Obstacle Avoidance using AI

An AI-based autonomous drone navigation system that performs indoor obstacle avoidance using Deep Learning and Reinforcement Learning in a simulation environment.

The project integrates:

Microsoft AirSim for drone simulation

TensorFlow for neural network models

OpenCV for image processing

The drone learns to navigate indoor environments and avoid obstacles using camera images.

📌 Project Overview

Autonomous UAV navigation in indoor environments is challenging due to:

Lack of GPS

Dynamic obstacles

Limited sensor data

This project solves the problem using computer vision and deep learning.

The drone captures images from its camera, processes them using a CNN model, and selects the best movement using Deep Q-Network (DQN) reinforcement learning.

🧠 System Architecture
Drone Camera
     │
     ▼
Image Capture
     │
     ▼
CNN Model
     │
     ▼
Feature Extraction
     │
     ▼
Reinforcement Learning (DQN)
     │
     ▼
Action Selection
     │
     ▼
Drone Movement
📂 Project Structure
UAV-indoor-obstacle-avoidance-based-on-AI-technique
│
├── dataset
│   ├── data.csv
│   └── imgs.zip
│
├── imgs
│   ├── dataset.png
│   ├── ensemble_architecture.png
│   ├── environment.png
│   ├── Model_ResNet08_accuracy.png
│   └── resnet08_architecture.png
│
├── models
│   ├── CNNModel.json
│   └── CNNWeight.hdf5
│
├── RL Module
│   └── src
│       ├── controller
│       │   ├── CNNController.py
│       │   ├── Controller.py
│       │   └── CNNModel.py
│       │
│       ├── utils
│       │
│       └── main.py
│
├── ResNet_UAV.ipynb
└── README.md
⚙️ Features

✔ Autonomous drone navigation
✔ Indoor obstacle avoidance
✔ Reinforcement Learning based control
✔ Convolutional Neural Network for vision
✔ AirSim drone simulation integration
✔ Deep learning-based decision making

🛠 Technologies Used

Python

TensorFlow

Keras

OpenCV

Microsoft AirSim

NumPy

Reinforcement Learning (DQN)

🚀 Installation
1️⃣ Clone the repository
git clone https://github.com/yourusername/UAV-indoor-obstacle-avoidance.git
cd UAV-indoor-obstacle-avoidance
2️⃣ Install dependencies
pip install airsim tensorflow keras opencv-python numpy
3️⃣ Install AirSim

Download Microsoft AirSim environment.

Recommended environment:

Blocks Environment

Download from:

https://github.com/microsoft/AirSim/releases

Run:

Blocks.exe
▶️ Running the Project

Navigate to the source folder:

cd "RL Module/src"

Run the main script:

python main.py
🧠 How It Works

The drone connects to the AirSim simulator

The drone arms and takes off

Camera images are captured from the drone

Images are processed using a CNN model

Reinforcement learning (DQN) predicts the next action

The drone moves accordingly to avoid obstacles

Example action selection:

dqn_predict = dqn.model.predict(img.reshape(1,144,256,3))
controller.take_action(np.argmax(dqn_predict))
📊 Model Architecture

The project uses a ResNet-8 CNN architecture trained on drone camera images.

The model learns to identify:

obstacles

free paths

safe navigation directions

Architecture visualization:

Input Image
   ↓
Convolution Layers
   ↓
Residual Blocks
   ↓
Feature Extraction
   ↓
Action Prediction
📈 Dataset

The dataset contains:

drone camera images

corresponding steering directions

Files:

dataset/data.csv
dataset/imgs.zip
🔮 Future Improvements

Possible enhancements:

Real-world drone deployment

Faster reinforcement learning training

Multi-drone coordination

SLAM-based navigation

YOLO-based obstacle detection

Autonomous path planning

# Vehicle-Edge Server Simulation with Object Detection and Route Planning

## Overview

This project demonstrates a 5G-inspired vehicle-edge server simulation that integrates edge computing to handle computationally intensive tasks. Using gRPC for communication, it showcases the following capabilities:

- **Object Detection**: Utilizing YOLOv5 to detect objects in images captured by the vehicle.
- **Route Planning**: Implementing the A* algorithm for efficient navigation.

## Project Demonstration

You can view a project demonstration video here:

[Project Demo](https://drive.google.com/file/d/12E35PFODAug7Wxw7jHCauiQ6RLrnpLoC/view?usp=sharing)

## Features

- **Real-Time Communication**: Leverages gRPC for low-latency, high-efficiency communication.
- **Edge Computing Integration**: Offloads heavy tasks to the edge server for optimal performance.
- **Scalability**: Designed to work in 5G environments with potential for multi-vehicle setups.

## System Components

### Vehicle Simulation:
- Captures images and sends them to the edge server.
- Requests route planning computations.

### Edge Server:
- Processes object detection using YOLOv5.
- Computes navigation routes using the A* algorithm.

### Communication Protocol:
- Uses gRPC and Protocol Buffers for efficient data serialization.

## Installation Steps

### Prerequisites
Ensure the following prerequisites are met:

- Python 3.8 or higher
- Required Python libraries:
  - `torch`
  - `opencv-python`
  - `grpcio`
  - `grpcio-tools`
  - `numpy`

### 1. Clone the Repository

```bash
git clone https://github.com/IIITV-5G-and-Edge-Computing-Activity/5G-Edge-Drive.git
cd 5G-Edge-Drive-master

# 2. Install Dependencies
pip install -r requirements.txt

# 3. Generate gRPC Files
python -m grpc_tools.protoc -I. --python_out=. --grpc_python_out=. vehicle_edge.proto

# 4. Start the Edge Server
python edge_server.py

# 5. Run the Vehicle Simulation
python vehicle.py




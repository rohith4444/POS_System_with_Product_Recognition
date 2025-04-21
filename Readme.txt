# Smart Point of Sale (POS) System with Product Recognition

## Project Overview

This project is a Smart Point of Sale (POS) system enhanced with computer vision capabilities for recognizing fruits and vegetables. The system combines:

1. **Computer Vision Recognition**: Using a custom-trained IRCNN (Inception Recurrent Convolutional Neural Network) model to identify produce without barcodes or labels
2. **POS Software**: A complete retail management system built with Python and Kivy framework
3. **Database Integration**: MongoDB for inventory and transaction management

The primary goal is to streamline the checkout process in grocery stores by automatically identifying produce when held in front of a camera, eliminating the need for manual product code entry or lookup.

## System Architecture

### 1. Computer Vision Component
- **Model**: IRCNN (Inception Recurrent Convolutional Neural Network)
- **Dataset**: Custom-curated dataset of fruits and vegetables
- **Training Framework**: TensorFlow/Keras
- **Input**: Images from camera feed
- **Output**: Product identification and pricing information

### 2. POS Software Component
- **Frontend**: Developed using Kivy framework for cross-platform GUI
- **Backend**: Python with MongoDB integration
- **User Roles**: 
  - Administrator (inventory management, reports, user management)
  - Operator (sales transactions)

## Features

### Admin Interface
- User management (add, update, remove users)
- Product management (add, update, remove products)
- Inventory management
- Sales analytics and reporting
- Product purchase analysis with visualization

### Operator Interface
- Product scanning/recognition
- Manual product code entry
- Shopping cart management
- Receipt generation
- Discount application

### Security
- Role-based access control
- Password hashing and authentication

## Installation and Setup

### Prerequisites
- Python 3.7 or higher
- MongoDB
- Required Python packages:
  - Kivy
  - TensorFlow/Keras
  - NumPy
  - Pandas
  - Matplotlib
  - pymongo

### Installation Steps

1. Clone the repository:
```
git clone https://github.com/your-username/smart-pos-system.git
```

2. Install required packages:
```
pip install -r requirements.txt
```

3. Set up MongoDB:
```
# Start MongoDB service
mongod --dbpath /path/to/db
```

4. Configure database connection in the application:
Update database connection parameters in relevant files if necessary.

5. Run the main application:
```
python POS/main.py
```

## Usage Guide

### Login
- The system starts with a login screen
- Use appropriate credentials based on your role:
  - Administrator: Full access to system features
  - Operator: Limited to sales operations

### Admin Workflow
1. Navigate to "Manage Products" to add/update inventory
2. Use "Product Analysis" to view sales trends
3. "Manage Users" allows adding/removing system users

### Operator Workflow
1. Start a new transaction
2. Scan products using camera or enter product codes manually
3. Apply discounts if necessary
4. Complete transaction and generate receipt

## AI Model Training

The IRCNN model was trained on a custom dataset with the following characteristics:
- 6,000 training images across 10 product categories
- 3,000 validation images
- 2,000 test images
- Image resolution: 256x256 pixels

The model architecture combines:
- Recurrent convolutional layers for feature extraction
- Inception blocks for multi-scale feature processing
- Global average pooling for classification

Training parameters:
- Batch size: 16
- Optimizer: SGD with learning rate of 0.01
- 50 epochs of training
- Data augmentation with normalization

The model achieved 90.05% accuracy on the test dataset.

## Future Improvements

- Real-time inventory updates based on sales
- Customer loyalty program integration
- Mobile application for inventory management
- Enhanced analytics dashboard
- Integration with payment processing systems
- Barcode scanning for packaged products
- Expanded product recognition categories

## Contributors

- Rohith Reddy Mandala

 

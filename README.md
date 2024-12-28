# Face Recognition Attendance System

This project implements a real-time face recognition-based attendance system using Python, OpenCV, and FaceNet. It enables user registration and face detection with embedding-based recognition.

## Features
- **User Registration:** Capture face images and store embeddings with SQLite database.
- **Face Recognition:** Match live face data against stored embeddings.
- **Efficient Storage:** Embeddings are saved in an NPZ file for quick access.

## Installation
1. Clone the repository and navigate to the project directory.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the program:
   ```bash
   python main.py
   ```

## Usage
- Press `c` to capture a face image during registration.
- Press `q` to quit capturing or recognition mode.
- Press `Esc` during recognition to exit.

## Requirements
- Python 3.7+
- OpenCV
- PyTorch
- FaceNet-PyTorch
- SQLite3

## Directory Structure
- `images/`: Stores captured user images.
- `attendance_system.db`: SQLite database for user data.
- `embeddings.npz`: Saved face embeddings and names.

## License
This project is licensed under the MIT License.


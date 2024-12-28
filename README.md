# Face Recognition Attendance System

A face recognition-based attendance system built using Python, OpenCV, MTCNN, and FaceNet for facial feature extraction. This system allows capturing user data (faces), storing embeddings, and performing face recognition in real-time for attendance tracking.

## Features

1. **Capture Faces and Generate Embeddings**: Capture multiple images of a user, extract facial embeddings, and store them in a database.
2. **Store User Data**: Store captured face images and their corresponding embeddings in a SQLite database.
3. **Face Recognition**: Detect and recognize faces in real-time using webcam feed, comparing them against stored embeddings.
4. **Attendance Tracking**: Identify and track users as they appear in the camera frame.

## Technologies Used

- **Python**: Programming language used for implementing the system.
- **OpenCV**: Used for capturing images and video streams from the webcam.
- **MTCNN**: For face detection.
- **FaceNet**: For generating facial embeddings.
- **SQLite**: For storing user data (name, image path).
- **NumPy**: For handling arrays and embeddings.
- **Torch**: Deep learning framework used for loading the FaceNet model.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/tusharpatil69/Face_Recognition_attendance_system
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Ensure you have a webcam connected to your system.

## Usage

### Capture Faces and Add New Users
Run the script and follow the prompts to capture face images and generate embeddings for a new user:

- Press `c` to capture an image for the new user.
- Press `q` to quit capturing.

### Face Recognition
After capturing face images for a user, you will be asked if you want to add a new user or start face recognition. If you choose to start face recognition, the system will begin detecting faces and matching them with stored users.

- Press `n` to stop detection and add a new user.
- Press `Esc` to exit face recognition.

## File Structure

- **attendance_system.db**: SQLite database storing user data (id, name, image path).
- **embeddings.npz**: File storing face embeddings for all users.
- **images/**: Directory where captured user images are saved.
- **main.py**: Main script for running the program.

## How It Works

1. **Face Detection**: The system uses MTCNN to detect faces in real-time from the webcam feed.
2. **Embedding Generation**: For each detected face, the system generates an embedding using the FaceNet model (InceptionResnetV1).
3. **Recognition**: When performing face recognition, the system compares the embedding of a detected face with stored embeddings. If a match is found, it identifies the user; otherwise, the face is labeled as "Unknown."

## Contributing

If you'd like to contribute to this project, feel free to fork the repository, create a branch, and submit a pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.


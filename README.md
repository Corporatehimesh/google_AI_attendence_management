# Attendance Management System Using Face Recognition

## Project Overview

Attendance Management System is an AI-powered attendance solution that automates student attendance using facial recognition technology.

The system consists of:

* Android Application (Java + XML)
* Flask Backend (Python)
* FaceNet Face Recognition
* MTCNN Face Detection
* Attendance Reporting System

The application supports:

* Student Registration
* Face Enrollment
* Live Attendance
* Group Attendance
* Attendance Report Export

---

# Project Repository

## Android Studio Source Code

Download Android Project Files:

https://drive.google.com/drive/folders/1J_AhVKXcMZY45Wt2NxqbbR4DBV7qyROX?usp=sharing

---

## Backend Source Code

Backend Flask files are available in this GitHub repository.

Main backend file:

```text
app.py
```

---

# Technologies Used

## Frontend

* Java
* XML
* Android Studio
* CameraX
* OkHttp

## Backend

* Python
* Flask
* OpenCV
* TensorFlow
* MTCNN
* FaceNet

## Storage

* Pickle Database
* CSV Files

---

# System Requirements

## Laptop / PC

* Windows 10 / 11
* Python 3.10+
* Android Studio
* Git

## Android Device

* Android 8.0+
* Camera Permission
* Same WiFi Network as Backend

---

# Backend Setup

## Step 1: Clone Repository

```bash
git clone YOUR_GITHUB_REPOSITORY
```

Open:

```text
AttendanceBackend
```

---

## Step 2: Install Python Packages

```bash
pip install flask
pip install tensorflow
pip install keras-facenet
pip install mtcnn
pip install opencv-python
pip install pillow
pip install numpy
pip install pandas
pip install scikit-learn
```

Or:

```bash
pip install -r requirements.txt
```

---

## Step 3: Run Backend

```bash
python app.py
```

Expected Output:

```text
Loading FaceNet...
Loading MTCNN...
Loading Database...
Students Loaded: XXX

Running on:
http://0.0.0.0:5000
```

---

# Android Setup

## Step 1

Download Android Studio project from:

https://drive.google.com/drive/folders/1J_AhVKXcMZY45Wt2NxqbbR4DBV7qyROX?usp=sharing

---

## Step 2

Open Android Studio

Select:

```text
Open Existing Project
```

Choose downloaded folder.

---

## Step 3

Allow Gradle Sync

Wait until:

```text
Gradle Build Successful
```

---

# Configure IP Address

The Android application communicates with the Flask backend using a local IP address.

Find current laptop IP:

Open Command Prompt:

```cmd
ipconfig
```

Locate:

```text
IPv4 Address
```

Example:

```text
192.168.1.37
```

---

Open:

```text
app/src/main/java/com/attendancemanagement/utils/ApiConfig.java
```

Update:

```java
public static final String BASE_URL =
"http://192.168.1.37:5000";
```

Replace with your own IP.

Example:

```java
public static final String BASE_URL =
"http://192.168.1.100:5000";
```

---

# Build APK

Android Studio:

```text
Build
↓
Build APK(s)
```

Install generated APK on device.

---

# Testing Procedure

## Student Registration

1. Open App
2. Click Add Student
3. Enter:

   * Name
   * Enrollment Number
   * Branch
   * Semester
   * Section
4. Click Face Verification
5. Capture all 5 face samples
6. Wait for upload completion

---

## Verify Face Samples

Open browser:

```text
http://YOUR_IP:5000/student_samples/STUDENT_NAME
```

Example:

```text
http://192.168.1.37:5000/student_samples/HIMESH%20RINCHHODIYA
```

Expected:

```json
{
  "count": 6
}
```

---

# Live Attendance Testing

1. Open Live Attendance
2. Allow Camera Permission
3. Face camera
4. Wait 2–5 seconds

Expected:

Known Student:

```text
✓ HIMESH RINCHHODIYA
```

Unknown Person:

```text
✗ UNKNOWN
```

Attendance automatically saved.

---

# Group Attendance Testing

Option 1:

```text
Capture Group Photo
```

Option 2:

```text
Select From Gallery
```

Expected:

* Multiple students detected
* Attendance marked automatically
* Recognition results displayed

---

# Attendance Records

Attendance stored in:

```text
attendance.csv
```

Example:

```csv
Name,Date,Time
HIMESH RINCHHODIYA,2026-06-24,09:10:05
```

---

# Features

* Student Management
* Face Enrollment
* Live Attendance
* Group Attendance
* Attendance History
* CSV Export
* Face Recognition
* Mobile Application
* Real-Time Detection

---

# Common Issues & Fixes

## App Cannot Connect To Server

Check:

* Laptop and phone connected to same WiFi
* Correct IP in ApiConfig.java
* Flask server running

Test:

```text
http://YOUR_IP:5000/students
```

Browser should open successfully.

---

## Camera Not Opening

Check:

```text
Settings
↓
Permissions
↓
Camera
↓
Allow
```

---

## Face Samples Not Uploading

Check backend terminal.

Expected:

```text
ADD FACE SAMPLE CALLED
NEW COUNT = X
```

---

## Student Showing UNKNOWN

Possible reasons:

* Poor lighting
* Face too far from camera
* Face samples not uploaded
* Incorrect threshold

Verify:

```text
/student_samples/STUDENT_NAME
```

---

## Group Photo Detects 0 Faces

Check:

* Image quality
* Face visibility
* Proper lighting

Use higher resolution images.

---

## Build Errors in Android Studio

Try:

```text
File
↓
Invalidate Caches
↓
Restart
```

Then:

```text
Build
↓
Clean Project
↓
Rebuild Project
```

---

# Future Enhancements

# The system can be further improved by implementing:

1.Cloud Database Integration
Use Firebase, MySQL, or MongoDB for centralized storage.


2.Anti-Spoof Detection
Detect printed photos or mobile screen attacks.


3.Teacher Authentication
Secure login system for teachers and administrators.


4.Real-Time Classroom Attendance
Continuous attendance monitoring without manual capture.


5.Advanced Deep Learning Models
Use ArcFace, InsightFace, or improved FaceNet models for higher accuracy.


6.Attendance Analytics Dashboard
Generate reports, graphs, and attendance statistics automatically.


7.Multi-Classroom Support
Manage multiple classes and departments simultaneously.


8.Cloud Deployment
Host backend on AWS, Azure, or Google Cloud for remote access.


9.Push Notifications
Notify students and faculty regarding attendance status.


10.Mobile Application Enhancements
Offline attendance mode.


11.Faster recognition.
Better user interface.


# One more recommendation: use requirements.txt file to GitHub. Then users can install everything with:

pip install -r requirements.txt

---

# Author

Himesh Rinchhodiya  & Team (+15)
Computer Science and Business Systems (CSBS)
Medicaps University
contact - 9685527886 













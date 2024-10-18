# D.Y Patil College of Engineering App

This is an Android application designed for D.Y Patil College of Engineering. The app features a home page displaying various departments of the college, a navigation system with two tabs (Home and Profile), and an image uploading feature that stores and retrieves images using Firebase.

# Features
  Home Page: Displays information and images of different departments of D.Y Patil College of Engineering.
  Navigation Tabs:
    Home Tab: Contains details about the college and its departments.
    Profile Button: Allows users to upload a profile image to Firebase, and fetches the stored image back 
    into the app.
  Firebase Integration:
    Image uploading and storage in Firebase.
    Fetches the stored profile image to display in the app.
# Screenshots
  ![1](https://github.com/user-attachments/assets/d9bb4dda-fa99-45a8-8dc8-555c16c32254)
![2](https://github.com/user-attachments/assets/38ac0060-d379-4d4b-9c29-03bfc06aee91)
![31](https://github.com/user-attachments/assets/afed6902-1ddb-405b-8c5f-67fc2eef4467)
![4](https://github.com/user-attachments/assets/0d2f93a8-a2ec-4b25-a329-44c252f1e7aa)


# Installation
To run the project locally, follow these steps:

Clone the repository:
1. Open the project in Android Studio.
2. Sync Gradle files and ensure you have the required dependencies, including Firebase.
3. Connect the app to Firebase by following Firebase Setup for Android.
4.Build and run the app on an emulator or a physical device.

# Requirements
  Android Studio: Arctic Fox or newer.
  Minimum SDK: 24 (Android 5.0 Lollipop).
  Firebase: Make sure you have a Firebase project set up with the Firebase Realtime Database or Firebase    Firestore and Firebase Storage.
  Internet Permission: Add this permission to your AndroidManifest.xml to enable internet access.
  xml

<uses-permission android:name="android.permission.INTERNET" />

# Folder Structure
![strcut](https://github.com/user-attachments/assets/01ba2b32-1626-43da-96ef-9831b838cc63)


app/
├── manifests/
├── java/
│   └── myapp.org.dyapp/
│       ├── ImageAdapter.java
│       ├── MainActivity.java
│       ├── splash_screen.java
│       └── studentid.java
│   └── myapp.org.dyapp (test)
├── res/
│   ├── anim/
│   ├── drawable/
│   │   ├── ai.jpg
│   │   ├── avatar.webp
│   │   ├── ce.webp
│   │   ├── comppp.jpeg
│   │   ├── dyp_background.xml
│   │   ├── dypatil.jpeg
│   │   ├── dypintuni1.jpg
│   │   ├── ee.png
│   │   ├── ic_eye_hidden.xml
│   │   ├── ic_eye_visible.xml
│   │   ├── ic_launcher_background.xml
│   │   ├── ic_launcher_foreground.xml
│   │   ├── information_technology.png
│   │   ├── profilebkg.png
│   │   ├── ra.png
│   │   ├── splash_screen.jpeg
│   ├── layout/
│   │   ├── activity_main.xml
│   │   ├── image_item.xml
│   │   ├── splash_screen.xml
│   │   ├── studentid.xml
│   └── menu/
│   │   └── values/
│   │       ├── strings.xml
│   │       └── colors.xml
└── build.gradle




# Code Overview
  XML Layouts
  activity_main.xml: The main layout containing the navigation and tabs (Home and Profile).
  image_item.xml: Displays the information and images about the college and its departments.
  splash_screen.xml: Contains the image upload functionality, allowing users to upload their profile         picture to Firebase and display it on their profile.
  
  Java Files
  MainActivity.java: Handles the navigation between the Home and Profile tabs.
  ImageAdapter.java: Manages the image uploading process, including storing and fetching the image from     Firebase.
  splash_screen: Display a runnig screen for a while.
  studentid: display student information
  FirebaseUtils.java: A utility class to handle Firebase operations such as uploading images to Firebase    Storage and fetching them.

# Firebase Setup
Firebase Storage: Used for storing profile images uploaded by the users.
Firebase Database (optional): You can store image metadata or other user information in Firebase Realtime Database or Firebase Firestore.
Ensure you add your google-services.json file in the app/ directory after setting up Firebase.

# How to Use
Navigate to Home Tab: View images and information about various departments of the D.Y Patil College of Engineering.
Upload Profile Image: In the Profile tab, users can upload their profile image. The image is stored in Firebase Storage and retrieved to display on the same screen.
Profile Image Fetching: On relaunching the app, the stored profile image is fetched from Firebase and displayed on the Profile tab.

# Dependencies
Add the following dependencies to your build.gradle:
    implementation 'androidx.appcompat:appcompat:1.7.0'
    implementation 'com.google.android.material:material:1.12.0'
    implementation 'androidx.constraintlayout:constraintlayout:2.1.4'
    implementation "androidx.navigation:navigation-ui:2.4.0"
    implementation 'com.google.firebase:firebase-database:21.0.0'
    implementation 'com.google.firebase:firebase-storage:21.0.1'
    testImplementation 'junit:junit:4.13.2'
    androidTestImplementation 'androidx.test.ext:junit:1.2.1'
    androidTestImplementation 'androidx.test.espresso:espresso-core:3.6.1'
    implementation 'de.hdodenhof:circleimageview:3.1.0'
    implementation 'com.github.bumptech.glide:glide:4.15.1'
    annotationProcessor 'com.github.bumptech.glide:compiler:4.15.1'
    implementation 'androidx.recyclerview:recyclerview:1.3.1'

# Future Improvements
Implement a login system for personalized user experience.
Add more information to the Home tab (e.g., courses offered, faculty information).
Expand the Profile tab to allow users to edit and update their personal details.
Implement offline storage for the images using Firebase offline persistence.

# Experiment 10: Data Sharing using Contacts Content Provider

## Student Details

**Name:** Tejas Sunil Waske  
**USN:** 25MCAR0189  
**Experiment No.:** 10

---

## Aim

To implement data sharing in Android by using the Contacts Content Provider.

---

## Objective

The objective of this experiment is to understand how Android applications can access and share data using Content Providers.

The application demonstrates accessing contact information from the device using the Contacts Content Provider and displaying the retrieved contact details.

---

## Concept / Technology Used

### Content Provider

A Content Provider is an Android component that manages and provides access to a shared set of application data.

It allows one application to access data managed by another application in a controlled manner.

Android provides several built-in Content Providers for accessing common data such as:

- Contacts
- Call logs
- Media
- Calendar
- Other shared data

---

### Contacts Content Provider

The Contacts Content Provider is used to access contact information stored on the Android device.

The application can query contact data using Android's Contacts Provider APIs.

The Contacts Provider contains information such as:

- Contact Name
- Phone Number
- Contact ID

---

### ContentResolver

`ContentResolver` is used by an Android application to communicate with a Content Provider.

The application uses:

```kotlin
contentResolver.query()
```

to request contact information from the Contacts Content Provider.

---

### Cursor

A `Cursor` is used to read the results returned by the Content Provider query.

The Cursor allows the application to move through the returned contact records and retrieve values from different columns.

---

### Runtime Permission

Accessing contacts requires the appropriate runtime permission.

The application uses:

```text
android.permission.READ_CONTACTS
```

The user must grant permission before the application can read contact information.

---

## Scenario

The application demonstrates data sharing by accessing contacts stored on the Android device.

When the application starts, it requests permission to read contacts.

After permission is granted, the application queries the Contacts Content Provider using `ContentResolver`.

The retrieved contact information is then displayed in the application.

### Application Flow

```text
                    Android Application
                            |
                            ↓
                       MainActivity
                            |
                            ↓
                  Request Contact Permission
                            |
                            ↓
                  READ_CONTACTS Permission
                            |
                  +---------+---------+
                  |                   |
                Allow                Deny
                  |                   |
                  ↓                   ↓
          ContentResolver          Permission
                  |                  Denied
                  ↓
        Contacts Content Provider
                  |
                  ↓
                 Query
                  |
                  ↓
                Cursor
                  |
                  ↓
          Contact Name / Number
                  |
                  ↓
            Display Contacts
```

---

## Software Requirements

- Android Studio
- Kotlin
- Android SDK
- Gradle
- Android Emulator or Physical Android Device

---

## Technologies Used

- Kotlin
- Contacts Content Provider
- ContentResolver
- Cursor
- Runtime Permissions
- READ_CONTACTS Permission
- XML Layout
- Android SDK

---

## Project Folder and File Structure

```text
MADExperiment10/
│
├── app/
│   │
│   ├── src/
│   │   │
│   │   └── main/
│   │       │
│   │       ├── java/
│   │       │   └── com/example/madexperiment10/
│   │       │       └── MainActivity.kt
│   │       │
│   │       ├── res/
│   │       │   └── layout/
│   │       │       └── activity_main.xml
│   │       │
│   │       └── AndroidManifest.xml
│   │
│   └── build.gradle.kts
│
├── gradle/
│   └── wrapper/
│
├── .idea/
├── .gitignore
├── build.gradle.kts
├── gradle.properties
├── gradlew
├── gradlew.bat
├── settings.gradle.kts
├── screenshot.png
└── README.md
```

---

## Important Files and Their Purpose

### MainActivity.kt

`MainActivity.kt` contains the main application logic.

It is responsible for:

- Requesting contact permission.
- Accessing the Contacts Content Provider.
- Using ContentResolver to query contacts.
- Reading contact information using Cursor.
- Displaying contact details to the user.
- Handling permission results.

---

### activity_main.xml

`activity_main.xml` defines the user interface of the application.

It contains the required views for displaying the contact information retrieved from the Contacts Content Provider.

---

### AndroidManifest.xml

`AndroidManifest.xml` contains the application configuration and declares the required contacts permission.

```text
android.permission.READ_CONTACTS
```

This permission allows the application to read contact information from the device.

---

### build.gradle.kts

This file contains the Android application build configuration and required dependencies.

---

# Working / Implementation

## 1. Launch Application

When the application starts, `MainActivity` is launched.

The application checks whether permission to read contacts has been granted.

---

## 2. Request Contact Permission

The application requests:

```text
READ_CONTACTS
```

permission from the user.

The user can either allow or deny access to contacts.

---

## 3. Access Contacts Content Provider

After permission is granted, the application uses the Android `ContentResolver` to access contact information.

The application queries the Contacts Content Provider.

---

## 4. Query Contact Data

The application retrieves contact information using a query operation.

Example:

```kotlin
contentResolver.query()
```

The query returns contact data through a Cursor.

---

## 5. Read Contact Data using Cursor

The Cursor is used to iterate through the returned contact records.

The application reads information such as:

```text
Contact Name
Phone Number
```

---

## 6. Display Contact Information

The retrieved contact information is displayed in the application interface.

Example:

```text
Contact Name: Tejas
Phone Number: 9876543210
```

The actual contact information depends on the contacts available on the device.

---

## 7. Permission Denied

If the user denies the contact permission, the application cannot access contact information.

The application displays an appropriate message indicating that contact permission is required.

---

# Test Cases

## Test Case 1: Request Contact Permission

### Test Objective

To verify that the application correctly requests permission to access contacts.

### Test Steps

1. Launch the application.
2. Observe the permission dialog.
3. Check the requested permission.
4. Allow contact access.

### Expected Result

The application should request `READ_CONTACTS` permission from the user.

### Actual Result

The application successfully requested contact permission.

### Status

**PASS ✅**

---

## Test Case 2: Retrieve and Display Contacts

### Test Objective

To verify that the application successfully retrieves contact information using the Contacts Content Provider.

### Test Steps

1. Launch the application.
2. Grant contact permission.
3. Allow the application to access contacts.
4. Observe the displayed contact information.

### Expected Result

The application should retrieve and display the available contacts from the device.

### Actual Result

The contact information was successfully retrieved from the Contacts Content Provider and displayed in the application.

### Status

**PASS ✅**

---

## Test Case 3: Verify Student Name and USN

### Test Objective

To verify that the student's name and USN are displayed correctly in the application.

### Test Data

**Name:** Tejas Sunil Waske

**USN:** 25MCAR0189

### Test Steps

1. Launch the application.
2. Grant contact permission.
3. Observe the displayed contact/application information.
4. Verify the student's name and USN.

### Expected Result

The application should correctly display:

```text
Name: Tejas Sunil Waske
USN: 25MCAR0189
```

### Actual Result

The student's name and USN were displayed successfully.

### Status

**PASS ✅**

---

# Output

The application successfully demonstrates data sharing using the Contacts Content Provider.

The application requests contact permission, accesses the Contacts Content Provider using ContentResolver, retrieves contact information using Cursor, and displays the contact details.

### Output Screenshot

<img width="1080" height="2358" alt="screenshot101 png" src="https://github.com/user-attachments/assets/3b5d59cd-e664-456d-a0e7-0bceb542203b" />
<img width="1080" height="2358" alt="screenshot102 png" src="https://github.com/user-attachments/assets/d38d99d9-29f0-49c7-bf51-04ee0671bfbf" />
<img width="732" height="1600" alt="screenshot103 png" src="https://github.com/user-attachments/assets/2f432d38-43d4-41b0-9533-e5221cffd5f8" />




---

# Steps to Run the Project

1. Open the project in Android Studio.
2. Allow Gradle synchronization to complete.
3. Connect an Android device or start an Android Emulator.
4. Make sure the device contains some contacts.
5. Select the application from the Run Configuration.
6. Click the **Run ▶** button.
7. Launch the application.
8. Grant the `READ_CONTACTS` permission.
9. Observe the retrieved contact information.
10. Verify that the contact details are displayed successfully.

---

# Requirements

## Hardware Requirements

- Laptop/Desktop
- Android Device or Android Emulator
- USB Cable if using a physical Android device
- Contacts stored on the Android device

## Software Requirements

- Android Studio
- Kotlin
- Android SDK
- Gradle

---

# Learning Outcomes

After completing this experiment, the following concepts were understood:

- Android Content Providers
- Contacts Content Provider
- ContentResolver
- Cursor
- Runtime Permissions
- READ_CONTACTS Permission
- Querying Contact Data
- Sharing Data Between Android Components
- Reading Contact Information
- Android XML Layouts

---

# Result

The Android application was successfully developed and executed to demonstrate data sharing using the Contacts Content Provider.

The application successfully requested contact permission, accessed the Contacts Content Provider, retrieved contact information using ContentResolver and Cursor, and displayed the retrieved data.

---

# Conclusion

The experiment successfully demonstrated how Android applications can share and access data using Content Providers.

The Contacts Content Provider was used to access contact information stored on the device. The application used ContentResolver to query the provider and Cursor to read the returned contact data.

Thus, the objective of implementing data sharing using the Contacts Content Provider was successfully achieved.

---

# Student Information

**Name:** Tejas Sunil Waske  
**USN:** 25MCAR0189

**Experiment:** Experiment 10 – Data Sharing using Contacts Content Provider

---

# GitHub Repository

**Repository Name:** MADExperiment10

**GitHub Link:**

twaske2-dotcom/ContactsProviderMAD10.git

---

# Reference

- Android Developers – Content Providers
- Android Developers – Contacts Provider
- Android Developers – ContentResolver
- Android Developers – Runtime Permissions

---

## Author

**Tejas Sunil Waske**

**USN:** 25MCAR0189

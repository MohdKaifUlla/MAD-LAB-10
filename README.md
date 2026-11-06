# Experiment 10 – Data Sharing Using Contacts Content Provider

## Student Information

- **Name:** Mohammed Kaif Ulla
- **USN:** 25MCAR0226
- **Subject:** Mobile Application Development (MAD)
- **Experiment No.:** 10

## Aim

To develop an Android application that demonstrates data sharing using the Contacts Content Provider and displays contact names stored on the device.

## Description

This Android application demonstrates how to access contact information using the Android Contacts Content Provider.

The application requests READ_CONTACTS permission from the user. After permission is granted, it uses ContentResolver to retrieve contact information and Cursor to read the contact records.

The retrieved contact names are displayed in a ListView using ArrayAdapter.

## Technologies Used

- Android Studio
- Kotlin
- XML
- Android SDK
- Content Provider
- ContentResolver
- Cursor
- ListView
- ArrayAdapter

## Features

- User-friendly Android interface.
- Runtime contact permission handling.
- Access contacts stored on the device.
- Retrieve contact names using ContentResolver.
- Display contacts using ListView.
- Handle permission denial.

## Permissions Used

```xml
<uses-permission android:name="android.permission.READ_CONTACTS" />
```

## Working Procedure

1. Launch the Android application.
2. Click the Load Contacts button.
3. The application checks READ_CONTACTS permission.
4. If permission is not granted, it requests permission.
5. ContentResolver queries the Contacts Content Provider.
6. Cursor reads the contact names.
7. ArrayAdapter connects data to ListView.
8. Contact names are displayed on the screen.

## Output Screenshots

### 1. Application Home Screen

<img width="1080" height="2358" alt="mad 10 a" src="https://github.com/user-attachments/assets/36abb1b3-07bd-46ae-8396-2a5559affac8" />

### 2. Contact Permission Request
<img width="1080" height="2358" alt="mad 10 b" src="https://github.com/user-attachments/assets/1ecd5d97-fce2-4417-968e-f5027f18ca05" />


### 3. Displaying Contact List

<img width="732" height="1600" alt="mad 10 c" src="https://github.com/user-attachments/assets/2a813e17-e64e-4593-af3e-87e36874d5f2" />


## Learning Outcomes

- Understanding Android Content Providers.
- Understanding ContentResolver.
- Retrieving data using Cursor.
- Implementing runtime permissions.
- Accessing device contacts.
- Displaying data using ListView and ArrayAdapter.

## Result

The Android application was successfully developed to demonstrate data sharing using the Contacts Content Provider.

## Conclusion

This experiment helped in understanding how Android applications access and share data through Content Providers. It also demonstrated runtime permissions and displaying retrieved contact information.

---

**Developed By:** Mohammed Kaif Ulla  
**USN:** 25MCAR0226

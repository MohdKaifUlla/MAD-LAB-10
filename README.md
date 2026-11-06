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

<!-- Add your application home screen screenshot here -->

![Application Home Screen](screenshots/home_screen.png)

### 2. Contact Permission Request

<!-- Add your permission request screenshot here -->

![Contact Permission](screenshots/contact_permission.png)

### 3. Displaying Contact List

<!-- Add your contact list screenshot here -->

![Contact List](screenshots/contact_list.png)

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

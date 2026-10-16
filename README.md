# 💬 Flutter Real-Time Chat App

A full-featured, real-time messaging application built with **Flutter**, powered by **Firebase** (Authentication, Firestore, Cloud Messaging) and **Supabase Storage**.

[![Flutter](https://img.shields.io/badge/Flutter-3.47+-02569B?logo=flutter&logoColor=white)](https://flutter.dev)
[![Dart](https://img.shields.io/badge/Dart-3.13+-0175C2?logo=dart&logoColor=white)](https://dart.dev)
[![Firebase](https://img.shields.io/badge/Firebase-Auth%20%7C%20Firestore%20%7C%20FCM-FFA611?logo=firebase&logoColor=white)](https://firebase.google.com)
[![Supabase](https://img.shields.io/badge/Supabase-Storage-3ECF8E?logo=supabase&logoColor=white)](https://supabase.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20iOS-brightgreen)](https://flutter.dev)

---

## ✨ Features

- 🔐 **User Authentication**: Secure email/password login and sign-up with real-time auth state listening (`FirebaseAuth`).
- ⚡ **Real-Time Messaging**: Instant message delivery and live stream updates using `Cloud Firestore`.
- 📸 **Profile Image Uploads**: User avatars captured via camera/gallery and stored in high-performance cloud storage (`Supabase`).
- 💬 **Smart WhatsApp-Style Chat UI**:
  - Dynamic speech bubbles with "speaking tail" styling.
  - User grouping: shows user avatar & username only on the first message of a consecutive sequence.
  - Adaptive alignment: right-aligned for sent messages, left-aligned for received messages.
- 🔔 **Push Notifications (FCM)**: Background and foreground push notifications powered by `Firebase Cloud Messaging`.
- 📱 **Safe Area & Edge-to-Edge Design**: Fully responsive layout adjusted for modern Android gesture bars and device notches.

---

## 🛠️ Tech Stack & Architecture

- **Framework**: [Flutter](https://flutter.dev/) (Dart)
- **Authentication**: [Firebase Authentication](https://firebase.google.com/docs/auth)
- **Database**: [Cloud Firestore](https://firebase.google.com/docs/firestore) (NoSQL Real-Time Database)
- **Push Notifications**: [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging)
- **Media Storage**: [Supabase Storage](https://supabase.com/storage)
- **Image Picker**: `image_picker` plugin

---

## 📂 Project Structure

```text
lib/
├── firebase_options.dart      # Auto-generated Firebase platform configuration
├── main.dart                  # App entry point, theme setup & Auth listener
├── screens/
│   ├── auth.dart              # Login & Sign-up screen with validation & avatar picker
│   ├── chat.dart              # Main chat room screen with FCM notification setup
│   └── splash.dart            # Loading splash screen during auth initialization
└── widgets/
    ├── chat_messages.dart     # StreamBuilder ListView rendering live messages
    ├── message_bubble.dart    # Custom chat bubbles with sequence grouping
    ├── new_message.dart       # Message input field with send action & Firestore integration
    └── user_image_picker.dart # Camera/Gallery image picker widget
```

---

## 🚀 Getting Started

### Prerequisites
- [Flutter SDK](https://docs.flutter.dev/get-started/install) installed (v3.13+)
- Android Studio / VS Code with Flutter extension
- An active [Firebase Project](https://console.firebase.google.com/)
- An active [Supabase Project](https://supabase.com/) for media storage

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Nouman-Khattak/flutter-chat-app.git
   cd flutter-chat-app
   ```

2. **Install dependencies:**
   ```bash
   flutter pub get
   ```

3. **Configure Firebase:**
   Ensure `google-services.json` is placed in `android/app/` and `firebase_options.dart` is configured.

4. **Run the app:**
   ```bash
   flutter run
   ```

5. **Build Release APK:**
   ```bash
   flutter build apk --split-per-abi
   ```

---

## 👤 Author

- **Nouman Farooq**
- Email: [nouman.khattak00@gmail.com](mailto:nouman.khattak00@gmail.com)
- GitHub: [@Nouman-Khattak](https://github.com/Nouman-Khattak)

---

## 📄 License

This project is licensed under the MIT License.

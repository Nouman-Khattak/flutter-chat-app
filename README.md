# 💬 Flutter Real-Time Chat App

A full-featured, real-time messaging application built with **Flutter**, powered by **Firebase** (Authentication, Firestore, Cloud Messaging) and **Supabase Storage**.

---

## 🚀 Features

- **🔐 User Authentication:** Secure email/password login and sign-up with real-time auth state listening (`FirebaseAuth`).
- **⚡ Real-Time Messaging:** Instant message delivery and live updates using `Cloud Firestore` streams.
- **🖼️ Profile Image Uploads:** User avatars captured via camera/gallery and stored in high-performance cloud storage (`Supabase`).
- **💬 Smart WhatsApp-Style Chat UI:**
  - Dynamic speech bubbles with "speaking tail" styling.
  - User grouping: shows user avatar & name only on the first message of a consecutive sequence.
  - Adaptive alignment: right-aligned for sent messages, left-aligned for received messages.
- **🔔 Push Notifications (FCM):** Background and foreground push notifications powered by `Firebase Cloud Messaging`.
- **📱 Safe Area & Edge-to-Edge Design:** Fully responsive layout adjusted for modern Android gesture bars and device notches.

---

## 🛠️ Tech Stack & Architecture

- **Framework:** [Flutter](https://flutter.dev/) (Dart)
- **Authentication:** [Firebase Authentication](https://firebase.google.com/docs/auth)
- **Database:** [Cloud Firestore](https://firebase.google.com/docs/firestore) (NoSQL Real-Time Database)
- **Push Notifications:** [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging)
- **Media Storage:** [Supabase Storage](https://supabase.com/storage)
- **Image Picker:** `image_picker` plugin

---

## 📂 Project Structure

```text
lib/
├── firebase_options.dart   # Auto-generated Firebase platform configuration
├── main.dart               # App entry point, theme setup, Auth listener
├── screens/
│   ├── auth.dart           # Login & Sign-up screen with form validation & image upload
│   ├── chat.dart           # Main chat room screen with FCM notification setup
│   └── splash.dart         # Loading screen during auth state initialization
└── widgets/
    ├── chat_messages.dart  # StreamBuilder ListView rendering live messages
    ├── message_bubble.dart # Custom chat bubbles with sequence grouping
    ├── new_message.dart    # Input field with send button & Firestore integration
    └── user_image_picker.dart # Camera/Gallery image picker widget
```

---

## ⚙️ Getting Started

### Prerequisites
- [Flutter SDK](https://docs.flutter.dev/get-started/install) installed
- An active [Firebase Project](https://console.firebase.google.com/)
- An active [Supabase Project](https://supabase.com/) for media storage

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/flutter_chat_app.git
   cd flutter_chat_app
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
   flutter build apk
   ```
   The APK will be generated at:
   `build/app/outputs/flutter-apk/app-release.apk`

---

## 👨‍💻 Author
Built with passion as part of mobile application development portfolio.

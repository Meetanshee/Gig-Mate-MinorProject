# GigMate

GigMate is a Flutter-based Smart Delivery Workforce Management System built with Firebase. It provides separate modules for delivery workers and administrators to manage orders, worker activity, delivery progress, earnings, wellness, and emergency alerts in realtime.

🔗 **Live Demo:** [gigmate-cffa5.web.app](https://gigmate-cffa5.web.app)
📦 **Repository:** [github.com/iamkrishsendhav/GigMate](https://github.com/iamkrishsendhav/GigMate)


## Project Overview

GigMate is designed to simplify delivery workforce operations through a connected digital platform.

The application includes two main modules:

- **Worker Module**: Workers can log in, view assigned orders, update delivery status, manage breaks, track earnings, view health status, and send SOS alerts.
- **Admin Module**: Admins can monitor workers, manage orders, view analytics, track live activity, and handle emergency alerts.


## Key Features

### Worker

- Worker login and signup
- Worker dashboard
- Assigned delivery orders
- Order status updates
- Navigation support
- Earnings and wallet screen
- Health status monitoring
- Break reminder system
- Order history
- Worker profile
- SOS emergency alert

### Admin

- Admin login with role verification
- Admin dashboard
- Order management
- Worker management
- Live worker tracking
- Analytics dashboard
- Admin profile
- SOS alert monitoring


## Tech Stack

- **Flutter**
- **Dart**
- **Firebase Authentication**
- **Cloud Firestore**
- **Firebase Core**
- **Firebase Storage**
- **Firebase Messaging**
- **Google Maps Flutter**
- **Geolocator**
- **Provider**
- **FL Chart**
- **URL Launcher**
- **Flutter Local Notifications**
- **Image Picker**


## Folder Structure

```text
lib/
  core/
    responsive.dart
    theme.dart

  models/
    order_model.dart
    user_model.dart

  services/
    order_service.dart
    user_service.dart
    worker_wellness_service.dart

  screens/
    role_selection_screen.dart
    worker_auth_options.dart
    worker_login_screen.dart
    worker_signup_screen.dart
    worker_dashboard.dart
    worker_profile_screen.dart
    delivery_list_screen.dart
    navigation_screen.dart
    health_status_screen.dart
    break_reminder_screen.dart
    earnings_wallet_screen.dart
    order_history_screen.dart

    admin/
      admin_login_screen.dart
      admin_dashboard.dart
      admin_orders_screen.dart
      admin_workers_screen.dart
      admin_analytics_screen.dart
      admin_live_tracking_screen.dart
      admin_profile_screen.dart

  widgets/
    custom_button.dart

  firebase_options.dart
  main.dart
```

## Firebase Collections

```
users       -> User information and role data
workers     -> Worker profile, status, and location data
orders      -> Delivery order details and status
earnings    -> Worker earning records
alerts      -> SOS and emergency alert records
admins      -> Admin profile data
```

## Order Status Flow

```
pending -> assigned -> accepted -> picked -> on_the_way -> delivered
```

---

## Getting Started

### Prerequisites

Make sure you have the following installed:

* Flutter SDK
* Dart SDK
* Android Studio or VS Code
* Firebase CLI
* Git

Check Flutter setup:

```
flutter doctor
```

### Installation

1. Clone the Repository

```
git clone https://github.com/iamkrishsendhav/GigMate.git
cd GigMate
```

2. Install Dependencies

```
flutter pub get
```

3. Configure Firebase

This project requires Firebase configuration.

Required setup:

* Enable Firebase Authentication
* Enable Cloud Firestore
* Add Firebase configuration files

Required files:

```
lib/firebase_options.dart
android/app/google-services.json
```

If Firebase is not configured, run:

```
flutterfire configure
```

### Run the App

Android

```
flutter run
```

Web

```
flutter run -d chrome
```

---

## Admin Role Setup

For admin login, the user must exist in Firebase Authentication and must have a Firestore document in the `users` collection with the admin role.

Example:

```json
{
  "role": "admin"
}
```

Worker users should have:

```json
{
  "role": "worker"
}
```

---

## Project Purpose

GigMate demonstrates a realtime delivery workforce management system using Flutter and Firebase. It focuses on order handling, worker tracking, role-based access, analytics, earnings, wellness monitoring, and emergency alert management.

---

## Author

**Krish Sendhav**
GitHub: [@iamkrishsendhav](https://github.com/iamkrishsendhav)
LinkedIn: [iamkrishsendhav](https://www.linkedin.com/in/iamkrishsendhav/)
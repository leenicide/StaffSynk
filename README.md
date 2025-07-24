# Workforce Management System (WMS)

**iOS-Optimized Flutter App** for shift scheduling, geofenced time tracking, and payroll automation. Built for Australia with Supabase + Firebase.

[![Flutter 3.19](https://img.shields.io/badge/Flutter-3.19-blue)](https://flutter.dev)
[![Supabase](https://img.shields.io/badge/Supabase-PostgreSQL%2015-green)](https://supabase.com)
[![Firebase Auth](https://img.shields.io/badge/Firebase-Auth%209-orange)](https://firebase.google.com)

<p align="center">
  <img src="assets/app_preview.gif" width="300" alt="App Preview">
</p>

## 🚀 Features

- **Role-Based Access Control** (Super Admin, Manager, Worker, Client)
- **Geofenced Clock-In/Out** with PostGIS validation
- **Realtime Rostering** with shift poaching
- **ABA Payroll Generation** via NestJS microservice
- **iOS-Optimized** (Cupertino widgets, CoreLocation)
- **AU Compliance** (APP Act, ATO reporting)

## 🛠 Tech Stack

| Layer              | Technology                          |
|--------------------|-------------------------------------|
| **Frontend**       | Flutter 3.19 (Dart 3)              |
| **State Mgmt**     | Riverpod 2.4                       |
| **Database**       | Supabase (PostgreSQL 15 + PostGIS) |
| **Auth**           | Firebase Authentication            |
| **Realtime**       | Supabase Realtime + FCM            |
| **Backend**        | NestJS (Payment Microservices)     |
| **DevOps**         | GitHub Actions + Fastlane          |

## 📂 Project Structure

```
lib/
├── core/
│   ├── auth/           # Firebase-Supabase bridge
│   ├── constants/      # RLS policies, enums
├── features/
│   ├── shifts/         # Rostering logic
│   ├── locations/      # Geofencing services
│   ├── payments/       # ABA generation
├── shared/
│   ├── ui/             # Platform widgets (Cupertino/Material)
│   ├── utils/          # Turf.dart geofence helpers
```

## 🖥 Development Setup

### Prerequisites
- Flutter 3.19+ (Channel stable)
- Xcode 15+ (for iOS builds)
- Supabase account
- Firebase project with iOS/Android apps

### Installation
1. Clone repo:
   ```bash
   git clone https://github.com/yourrepo/wms-flutter.git
   cd wms-flutter
   ```
2. Install dependencies:
   ```bash
   flutter pub get
   ```
3. Configure environment:
   ```bash
   cp .env.example .env
   # Fill Supabase/Firebase keys
   ```

## 🔧 Team Workflow

### Branch Strategy
- `main` → Production (protected)
- `feat/*` → Feature branches
- `ios/*` → iOS-specific changes
- `android/*` → Android adaptations

### Code Standards
- **Dart**: Effective Dart + `pedantic` linter
- **API Contracts**: OpenAPI specs in `/api-schema`
- **Commit Messages**: Conventional Commits

## 📱 Build Targets

| Platform  | Key Tools                  |
|-----------|----------------------------|
| **iOS**   | Xcode, TestFlight       |
| **Android**| Android Studio, Firebase|

## 🚨 Troubleshooting

**Common Issues**:
- `Missing GoogleService-Info.plist` → Run `flutterfire configure`
- `PostGIS function errors` → Verify Supabase extensions
- `Background location fails` → Check `Info.plist` permissions

## 📄 Documentation

- [Supabase Schema](docs/Supabase_Schema.md)
- [Firebase Setup Guide](docs/Firebase_Setup.md)
- [ABA Generation Spec](docs/Payroll_Spec.md)

## 📬 Contact

**Tech Lead**: leena@synkflow.cloud
**Backend Owner**: hashir@synkflow.cloud

---

<p align="center">
  <sub>Built with ❤️ for Ayaz Latif</sub>
</p>

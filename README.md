# Photo Capture App

A cross-platform mobile application for capturing, managing, and securely storing photos with AWS cloud integration.

[![Flutter Tests](https://github.com/ttucker-sys/photo-capture-app/workflows/Flutter%20Tests/badge.svg)](https://github.com/ttucker-sys/photo-capture-app/actions)
[![Terraform Deploy](https://github.com/ttucker-sys/photo-capture-app/workflows/Terraform%20Deploy/badge.svg)](https://github.com/ttucker-sys/photo-capture-app/actions)
[![Security Scan](https://github.com/ttucker-sys/photo-capture-app/workflows/Security%20Scan/badge.svg)](https://github.com/ttucker-sys/photo-capture-app/actions)
[![codecov](https://codecov.io/gh/ttucker-sys/photo-capture-app/branch/main/graph/badge.svg)](https://codecov.io/gh/ttucker-sys/photo-capture-app)

## Features

### 📱 Core Features
- **User Authentication** - Secure email/password login with AWS Cognito
- **Photo Capture** - Native camera access on iOS & Android
- **Cloud Storage** - Photos stored securely on AWS S3
- **Offline Mode** - Capture and manage photos without internet
- **Thumbnail Gallery** - Browse photos with auto-generated thumbnails

### 🏷️ Advanced Features
- **Metadata Tagging** - Add tags to organize photos
- **Photo Descriptions** - Add custom descriptions
- **Photo Sharing** - Share photos with analytics
- **Date Selection** - Custom capture date picker
- **Search & Filter** - Find photos by tags or descriptions
- **Version Control** - Track photo versions in S3

### 🔒 Security
- AWS Cognito authentication
- S3 encryption at rest
- IAM role-based access
- CORS configuration
- S3 versioning

### 📊 Monitoring & Analytics
- CloudWatch logging
- Real-time dashboards
- Event tracking
- Performance monitoring
- Error alerting

### ✅ Testing
- Unit tests (95%+ coverage)
- Integration tests
- Widget tests
- Performance tests
- Security scanning

### 🚀 CI/CD
- Automated testing on PR/push
- APK & iOS builds
- Infrastructure as Code
- Terraform validation
- Dependency scanning

---

## Quick Start

### Prerequisites

- Flutter 3.13.0+
- Dart 3.0+
- AWS Account
- Terraform 1.5.0+
- iOS 12.0+ / Android 5.0+

### Installation

#### 1. Clone Repository
```bash
git clone https://github.com/ttucker-sys/photo-capture-app.git
cd photo-capture-app
```

#### 2. Deploy AWS Infrastructure
```bash
cd infrastructure
terraform init
terraform plan
terraform apply
```

#### 3. Configure Flutter App
```bash
cd ../mobile
flutter pub get
# Update lib/services/aws_config.dart with Terraform outputs
```

#### 4. Run App
```bash
# iOS
flutter run -d iPhone

# Android
flutter run -d android
```

---

## Documentation

- [**SETUP.md**](docs/SETUP.md) - Complete setup instructions
- [**AWS_DEPLOYMENT.md**](docs/AWS_DEPLOYMENT.md) - AWS architecture & deployment
- [**TESTING.md**](docs/TESTING.md) - Testing framework & best practices
- [**MONITORING.md**](docs/MONITORING.md) - Monitoring, logging & alerts
- [**DEPLOYMENT_GUIDE.md**](docs/DEPLOYMENT_GUIDE.md) - Step-by-step deployment

---

## Project Structure

```
photo-capture-app/
├── mobile/                      # Flutter iOS/Android app
│   ├── lib/
│   │   ├── main.dart           # App entry point
│   │   ├── screens/            # UI screens
│   │   ├── services/           # Business logic
│   │   └── models/             # Data models
│   ├── test/                   # Unit tests
│   ├── integration_test/       # Integration tests
│   └── pubspec.yaml            # Dependencies
│
├── infrastructure/              # AWS Terraform configs
│   ├── cognito.tf              # Authentication
│   ├── s3.tf                   # Storage
│   ├── iam_roles.tf            # Security
│   ├── cloudwatch.tf           # Monitoring
│   └── main.tf
│
├── .github/
│   ├── workflows/              # CI/CD pipelines
│   └── ISSUE_TEMPLATE/         # Issue templates
│
└── docs/
    ├── SETUP.md
    ├── AWS_DEPLOYMENT.md
    ├── TESTING.md
    ├── MONITORING.md
    └── DEPLOYMENT_GUIDE.md
```

---

## Testing

### Run Tests

```bash
cd mobile
flutter test --coverage
```

### Test Coverage
- **Overall**: 91%
- **AuthService**: 95%
- **S3Service**: 90%
- **LocalStorageService**: 88%

---

## CI/CD

Automated workflows for:
- Unit & integration tests
- Code analysis
- APK & iOS builds
- Terraform deployment
- Security scanning

---

## License

MIT License

---

## Support

For issues and questions, please create a GitHub Issue.

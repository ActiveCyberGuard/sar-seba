# 🌾 Sar Seba — Smart Fertilizer Support System

Sar Seba is a simple web-based agricultural support system designed to help farmers record crop and fertilizer-related information and receive useful agricultural guidance.

The project uses **Firebase Firestore** as a shared cloud database, allowing submitted information to be stored centrally instead of remaining only in a user's browser.

---

## 📌 Project Overview

Farmers often need simple and accessible tools to record crop-related information and get fertilizer guidance.

**Sar Seba** provides a simple interface where users can submit agricultural information such as:

- Division
- Crop
- Season
- Year
- Land Area
- Fertilizer Information

The submitted information is stored in **Firebase Cloud Firestore**.

---
Live link:https://activecyberguard.github.io/sar-seba/
## ✨ Features

- 🌾 Simple and user-friendly agricultural interface
- 📝 Crop and fertilizer information submission
- ☁️ Shared cloud database using Firebase Firestore
- 🔐 Firestore security rules
- 📊 Centralized data storage
- 📱 Responsive web interface
- 🌐 Can be deployed using GitHub Pages
- 💾 Data can be accessed from different browsers/devices

---

## 🛠️ Technologies Used

| Technology       | Purpose                  |
|------------------|---------------------------|
| HTML5            | Web page structure        |
| CSS3             | User interface and styling|
| JavaScript       | Application logic         |
| Firebase         | Cloud backend              |
| Cloud Firestore  | Shared database             |
| Git              | Version control            |
| GitHub           | Source code hosting        |
| GitHub Pages     | Web hosting                |

---

## 🏗️ System Architecture

```text
              ┌──────────────────────┐
              │      Farmer/User     │
              └──────────┬───────────┘
                          │
                          ▼
              ┌──────────────────────┐
              │    Sar Seba Website  │
              │    HTML/CSS/JS       │
              └──────────┬───────────┘
                          │
                          ▼
              ┌──────────────────────┐
              │   Firebase Firestore │
              │     demand_log       │
              └──────────┬───────────┘
                          │
                          ▼
              ┌──────────────────────┐
              │   Shared Cloud Data  │
              └──────────────────────┘
```

---

## 🔥 Firebase Configuration

The project is connected to Firebase using the Firebase Web SDK.

The application uses:

- **Firebase Project:** Sar Seba
- **Firestore Collection:** `demand_log`

Firebase configuration is included in the application code through the `FIREBASE_CONFIG` object.

> **Note:** Firebase Web API keys are designed to be used in client-side applications. Access to Firestore data is controlled through Firebase Security Rules.

---

## 🔐 Firestore Security Rules

The project uses Firestore rules to control access to submitted records.

Current behavior:

| Action                  | Allowed? |
|--------------------------|----------|
| Read existing records    | ✅ Allowed |
| Create new records        | ✅ Allowed (when required fields are provided) |
| Update existing records   | ❌ Not allowed |
| Delete existing records   | ❌ Not allowed |

This helps prevent previously submitted records from being modified or deleted by clients.

---

## 📂 Project Structure

```
sar-seba/
│
├── index.html
│
└── README.md
```

---

## 🚀 How to Run Locally

**1. Clone the repository**
```bash
git clone https://github.com/ActiveCyberGuard/sar-seba.git
```

**2. Open the project folder**
```bash
cd sar-seba
```

**3. Run the project**

Open `index.html` in a web browser.

For better local development, the project can also be opened using VS Code Live Server.

---

## ☁️ Firebase Setup

To connect the project with Firebase:

1. Create a Firebase project.
2. Create a Web App.
3. Enable Cloud Firestore.
4. Copy the Firebase Web configuration.
5. Add the configuration to `FIREBASE_CONFIG`.
6. Configure Firestore Security Rules.
7. Run the web application.
8. Submit a sample record.
9. Verify the record from **Firestore Database → Data**.

---

## 🧪 Testing

The application can be tested by submitting sample agricultural information.

**Example:**

- Division: Dhaka
- Crop: Rice
- Season: Aman
- Year: 2026
- Land Area: 2 Acres
- Fertilizer: Urea

After submission, the information should be stored inside:

```
Firestore
   └── demand_log
        └── Document
```

The application can also be tested from different browsers/devices to verify that data is stored centrally in Firebase.

---

## 🔄 Data Flow

```text
User enters information
        ↓
   Submit form
        ↓
JavaScript processes data
        ↓
Firebase Firestore
        ↓
demand_log collection
        ↓
 Data stored in cloud
```

---

## 🌐 Deployment

The project can be deployed using GitHub Pages.

**Deployment flow:**

```text
Local Project
      ↓
     Git
      ↓
GitHub Repository
      ↓
GitHub Pages
      ↓
Live Website
```

---

## 🔮 Future Improvements

Possible future improvements include:

- 👨‍🌾 Farmer account/login system
- 📱 SMS notification
- 💬 WhatsApp-based farmer communication
- 🌦️ Weather information
- 🌱 Crop-specific fertilizer recommendations
- 📊 Agricultural data dashboard
- 🔔 Farmer notifications
- 🗺️ Location-based agricultural services
- 🔐 Firebase Authentication
- 🤖 AI-based agricultural recommendations

---

## 👨‍💻 Project

- **Project Name:** Sar Seba
- **Type:** Web-Based Agricultural Support System
- **Backend:** Firebase Firestore
- **Frontend:** HTML, CSS & JavaScript

---

## 📄 License

This project is developed for educational and learning purposes.

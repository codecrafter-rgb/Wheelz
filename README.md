# 🚲 Wheelz

**Wheelz** is a bike rental management system consisting of a **mobile application for renters** and an **administrative interface for managing the rental system**.

The application allows users to find nearby available bicycles, rent them using QR codes, track active and previous rentals, and report bicycle issues. Administrators can manage bicycles, monitor rentals, and review reported issues.

---

## 🛠️ Tech Stack

### Mobile Application

* **React Native**
* **Expo**
* **Expo Router**
* **Zustand**
* **OpenLayers**

### Backend

* **Node.js**
* **Express.js**
* **REST API**

### Development

* **JavaScript / TypeScript**
* **Git & GitHub**

---

## 📸 Screenshots

### Mobile Application

<!-- Replace these placeholders with actual screenshots -->

## 📸 Screenshots

| Homepage | Dashboard |
|:---:|:---:|
| ![Homepage](homepage.png) | ![Dashboard](dashboard.png) |

| Map | Rental History |
|:---:|:---:|
| ![Map](map.png) | ![History](history.png) |

---

## ✨ Features

### 👤 Renter

Renters access Wheelz through the mobile application.

* 🔐 **Registration & Login**

  * Create a new account
  * Log in and log out
* 👤 **Profile Management**

  * View personal information
  * Edit personal information
* 🗺️ **Browse Available Bicycles**

  * View nearby available bicycles on an interactive map
  * Automatically detect the user's current location
  * Manually enter a location
  * View designated parking locations
  * View bicycle details
* 📱 **QR Code Rental**

  * Scan the QR code attached to a bicycle
  * Start a rental directly from the mobile application
* 🚴 **Active Rental**

  * Track the current rental
  * View rental information
  * Finish the current rental
* 📋 **Rental History**

  * View previous rentals
* ⚠️ **Report Bicycle Issues**

  * Report irregularities or problems with a bicycle
* 🔔 **Rental Notifications**

  * Receive notifications related to rentals

### 🛠️ Administrator

Administrators access the system through a desktop interface.

* 🔐 Login & Logout
* 🚲 **Bicycle Management**

  * Add new bicycles
  * Edit existing bicycles
* 📋 **Rental Management**

  * View all rentals
* ⚠️ **Issue Management**

  * View reported bicycle issues

---

## 🗺️ How It Works

### 1. Find a Bicycle

After logging in, the renter can view available bicycles around their current location.

The application displays available bicycles and permitted parking locations on an interactive map.

### 2. Choose a Bicycle

Selecting a bicycle displays information such as:

* 📍 Exact location
* 🚲 Bicycle type
* 💰 Rental price
* 🅿️ Nearest permitted parking location

### 3. Scan & Rent

The renter scans the **QR code** attached to the selected bicycle using their phone's camera.

Once confirmed, the rental begins.

### 4. Track the Rental

While the rental is active, the user can monitor the current rental through the application.

### 5. Finish the Rental

The user can finish the rental when they reach an appropriate parking location.

The completed rental is then added to their rental history.

### 6. Report Problems

If a bicycle has a malfunction or other irregularity, the renter can submit a report through the application.

Administrators can review these reports through the administrative interface.

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │       Backend       │
                    │      REST API       │
                    └──────────┬──────────┘
                               │
                 ┌─────────────┴─────────────┐
                 │                           │
        ┌────────▼────────┐        ┌────────▼────────┐
        │  Mobile App     │        │  Admin Interface │
        │      📱         │        │       🖥️         │
        │                  │        │                  │
        │     Renter      │        │  Administrator   │
        └──────────────────┘        └──────────────────┘
```

---

## 👥 User Roles

| Role              | Platform    | Main Responsibilities                                 |
| ----------------- | ----------- | ----------------------------------------------------- |
| 👤 Renter         | 📱 Mobile   | Find and rent bicycles, manage rentals, report issues |
| 🛠️ Administrator | 🖥️ Desktop | Manage bicycles, rentals and reported issues          |

---

## 📱 Main User Flow

```text
┌─────────────┐
│ Register /  │
│    Login    │
└──────┬──────┘
       │
       ▼
┌──────────────────┐
│   Main Screen    │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│   Find Bicycles  │
│       🗺️         │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│ Select Bicycle   │
│       🚲         │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│   Scan QR Code   │
│       📱         │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│  Active Rental   │
│       🚴         │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│  Finish Rental   │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│ Rental History   │
│       📋         │
└──────────────────┘
```

---

## 👨‍💼 Administrator Flow

```text
Login
  │
  ▼
Admin Dashboard
  │
  ├── 🚲 Manage Bicycles
  │      ├── Add Bicycle
  │      └── Edit Bicycle
  │
  ├── 📋 View Rentals
  │
  └── ⚠️ View Reported Issues
```

---

## 📍 Maps & Location

Wheelz uses the user's location to provide an overview of nearby bicycles.

The map displays:

* 🚲 Available bicycles
* 🅿️ Permitted parking locations
* 📍 User's current location

Users can also manually provide a location when automatic location detection is unavailable or undesirable.

---

## 🔒 Authentication

The system supports authentication for both user types.

Users provide:

* Username
* Password

After successful authentication, the appropriate application interface is displayed according to the user's role.

Invalid credentials result in a generic login error, allowing the user to retry or register a new account.

---

## 📂 Project Structure

```text
Wheelz/
├── mobile/
│   ├── app/
│   ├── components/
│   ├── store/
│   └── ...
│
├── backend/
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   └── ...
│
├── admin/
│   └── ...
│
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

* [Node.js](https://nodejs.org/)
* npm
* Expo CLI / Expo Go
* Git

### Clone the repository

```bash
git clone <repository-url>
cd Wheelz
```

### Install dependencies

```bash
npm install
```

### Start the application

```bash
npx expo start
```

The mobile application can then be opened using **Expo Go** or an Android/iOS emulator.

> Backend configuration and environment variables may be required depending on the current project setup.

---

## 🎯 Project Goals

Wheelz aims to provide a simple and intuitive bicycle rental experience while giving administrators the tools required to operate and monitor the rental system.

The system focuses on:

* **Simple bicycle discovery**
* **Fast QR-based rentals**
* **Transparent rental tracking**
* **Easy issue reporting**
* **Centralized bicycle management**
* **Clear separation between renter and administrator functionality**

---

## 🗺️ Future Improvements

Potential future improvements include:

* 💳 Online payments
* 🔔 Push notifications
* ⭐ Bicycle ratings
* 📊 Advanced administrator analytics
* 🧭 Route navigation to bicycles and parking locations
* 🔎 Bicycle filtering and search
* 📈 Rental statistics and reports
* 🔧 Automated bicycle maintenance tracking

---

## 📄 Project

**Wheelz — Bike Rental Management System**

A software development project combining a mobile bicycle rental experience with an administrative management platform.

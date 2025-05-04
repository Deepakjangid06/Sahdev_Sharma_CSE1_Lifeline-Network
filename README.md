# Life Line Network - Emergency Based platform.

## Team Members
- Deepak(2401010085)
- Devansh Jain(2401010167)
- Tanmay Dixit(2401010120)

 

## Short Project Description
- Emergency Medical Service app based web — a smart and life-saving platform designed to connect patients, ambulance drivers, and hospitals during medical emergencies.

## Video Explanation
- https://drive.google.com/file/d/1j0I3DK3wBKWBeMTDuZ4-Y-AD9_4r2pru/view?usp=drivesdk


## Project Report
- 



## 📑 Table of Contents
- [Overview](#-overview)  
- [Features](#-features)  
   - [Emergency Services (No Login Required)](#-emergency-services-no-login-required)  
   - [Patient Features](#-patient-features)  
   - [Ambulance Driver Features](#-ambulance-driver-features)  
   - [Hospital Features](#-hospital-features)  
- [Notifications](#-notifications)  
- [Privacy & Security](#-privacy--security)  
- [Future Development](#-future-development)
- [Set-Up this Project in your application/machine]   
- [Tech Stack](#-TechStack)
- [Development Setup](#-development-setup)
- [Web Setup](#-web-setup)
- [Project Structure](#-project-structure) 
- [Support](#-support)  
- [License](#-license)

---

## 📌 Overview

This app based web facilitates emergency assistance by:
- Allowing patients to request ambulances and locate nearby hospitals quickly
- Enabling drivers to manage and respond to emergency requests
- Helping hospitals prepare for incoming patients with timely updates

Currently, this application works entirely on the **frontend**, with backend functionality planned in future releases. The **Map API** is fully integrated and functional.

---

## 🚨 Emergency Services (No Login Required)

- **Emergency Button**
  - Call an ambulance to your location
  - Find nearby hospitals with available services
- **Uses your real-time location** (with permission)
- **Provides ETA and driver info** once ambulance is assigned

---

## 👤 Patient Features

- Register and log in using your phone number and OTP
- Add personal info, medical history, and emergency contacts
- View past emergency requests
- Access emergency services with pre-filled details

---

## 🚑 Ambulance Driver Features

- Register with license and ambulance details
- Accept or reject emergency requests
- Track location, toggle availability, and view patient info
- Choose appropriate hospital and complete assignments

---

## 🏥 Hospital Features

- Register hospital with services and emergency contact info
- Update availability status
- Receive notifications about incoming patients
- Track estimated arrival time and patient details

---

## 🔔 Notifications

- **Patients:** Receive updates about ambulance arrival, driver info, and hospital selection  
- **Drivers:** Get notified about emergency requests and hospital responses  
- **Hospitals:** Alerts about incoming patients, ambulance details, and condition (when available)

---

## 🔒 Privacy & Security

- Location only accessed during emergency requests
- Medical data shared only with authorized parties
- All data encrypted and securely stored
- Users can delete their account and data at any time

---

## 🚧 Future Development

### 🔙 Backend Expansion
- Complete backend logic using Node.js/Express or Django
- Implement database interactions (MongoDB, PostgreSQL, Firebase)
- Enhance authentication, session handling, and error management


### 📡 Real-Time Functionality
- Add WebSocket or Firebase support for:
- Real-time ambulance tracking
- Live request status updates
- Hospital notifications
    
### 🔐 Security & Compliance
- Implement JWT/OAuth2 authentication
- Encrypt all sensitive data (medical, personal)
- Ensure GDPR and HIPAA compliance

  
### 🔗 Third-party & Device Integration
- Connect with health insurance APIs and national health records
- Explore IoT devices and wearables for emergency triggers
- Integrate with smartwatch and biometric sensors in the future


## Set-Up this Project in your application/machine


## 🛠️ Tech Stack

- **Frontend**: React 19, TypeScript, Vite, Tailwind CSS, Headless UI
- **Backend**: Node.js, Express, TypeScript
- **Database**: MongoDB (upcoming)
- **Authentication**: JWT


## 🔧 Development Setup

The project consists of three main components that can be developed separately or together:
1. **Frontend** - Next.js
2. **Backend** -  Node.js. is working but other  features like  flask and other requirement .. We impliment in future our project).
3. **Api Server** - Google Maps API Key


### Prerequisites

Before starting, ensure the following tools are installed on the laptop:

1. **Node.js** - (LTS version recommended): Download Node.js(at least)

2. Code Editor:

Install a code editor like Visual Studio Code from VS Code Official Website.


## Web setup

#### 1. Clone Repository
```bash
[git clone https://github.com/SAHDEVSHARMA/Sahdev_Sharma_CSE1_Lifeline-Network.git)
cd Sahdev_Sharma_CSE1_Lifeline-Network
```

#### 2. Install Dependencies
```bash
npm install
```
then 
```
npm install --legacy-peer-deps
```
if error,occur
```
npm audit fix
    or
npm audit --force
```
then 
```
npm run dev
```
ensure dev script recoginse your laptop if not then,run
```
npm install --save-dev nodemon
```
after that,
```
npm run dev
```


## 📁 Project Structure

```
updated-life-line-network/
├── public/                     # Static assets (images, icons, etc.)
│   ├── favicon.ico
│   ├── logo.png
│   └── ...
├── src/                        # Source code for the entire application
│   ├── app/                    # Frontend application (Next.js 13+ routing)
│   │   ├── emergency/          
│   │   │   ├── nearby-hospitals/
│   │   │   │   ├── page.tsx          # Nearby Hospitals page component
│   │   │   │   ├── styles.css        # Page-specific styles (optional)
│   │   │   │   └── index.test.tsx    # Unit tests for the page
│   │   ├── layout.tsx          # Root layout for the app
│   │   ├── globals.css         # Global CSS styles
│   │   └── page.tsx            # Main entry point (e.g., homepage)
│   ├── components/             # Reusable UI components
│   │   ├── Header.tsx          
│   │   ├── Footer.tsx          
│   │   ├── HospitalCard.tsx    
│   │   ├── Map.tsx             
│   │   └── ...
│   ├── hooks/                  # Custom React hooks
│   │   ├── useFetch.ts         
│   │   ├── useGeolocation.ts   
│   │   └── ...
│   ├── lib/                    # Shared utilities
│   │   ├── api.ts              
│   │   ├── geoUtils.ts         
│   │   └── ...
│   ├── styles/                 
│   │   ├── variables.css       
│   │   ├── mixins.css          
│   │   └── ...
│   ├── types/                  
│   │   ├── hospital.ts         
│   │   └── ...
│   ├── backend/                # Backend application (Node.js/Express)
│   │   ├── controllers/        
│   │   │   ├── hospitalController.ts
│   │   │   └── userController.ts
│   │   ├── models/             
│   │   │   ├── hospitalModel.ts 
│   │   │   └── userModel.ts     
│   │   ├── routes/             
│   │   │   ├── hospitalRoutes.ts 
│   │   │   └── userRoutes.ts     
│   │   ├── services/           
│   │   │   ├── hospitalService.ts 
│   │   │   └── userService.ts     
│   │   ├── middlewares/        
│   │   │   ├── authMiddleware.ts 
│   │   │   └── errorMiddleware.ts 
│   │   ├── utils/              
│   │   │   ├── logger.ts         
│   │   │   └── ...
│   │   ├── config/             
│   │   │   ├── dbConfig.ts       
│   │   │   ├── envConfig.ts      
│   │   │   └── serverConfig.ts   
│   │   ├── app.ts              
│   │   └── server.ts           
│   └── tests/                  
│       ├── components/         
│       ├── hooks/              
│       ├── controllers/        
│       ├── services/           
│       └── ...
├── .env                        
├── .gitignore                  
├── next.config.js              
├── package.json                
├── tsconfig.json               
├── README.md                   
└── Dockerfile
```
## 🛠️ Support

For help or to report issues, contact us:

- 📧 Email: [support@emergency-medical-app.com](mailto:support@emergency-medical-app.com)  
- 📞 Phone: 1-800-EMERGENCY

---

## 📄 License

This project is currently under development and not licensed for public use yet. Licensing details will be added in future releases.


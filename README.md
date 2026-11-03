# 🚀 Fasto - Vehicle Rental Platform

A modern, full-stack vehicle rental platform built with React, TypeScript, Firebase, and Tailwind CSS. Rent bikes and scooters for your trips with flexible return options and smart fleet management.

![Fasto](https://img.shields.io/badge/React-18-blue) ![TypeScript](https://img.shields.io/badge/TypeScript-4.9-blue) ![Firebase](https://img.shields.io/badge/Firebase-12.4-orange) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.3-cyan)

## 🌟 Features

### 🎯 Core Features
- **🚗 Vehicle Rental Platform** - Rent bikes and scooters for your trips
- **💰 Affordable Pricing** - Starting from just ₹25/hour
- **📍 Flexible Return Locations** - Return vehicles anywhere
- **👥 Dual User System** - Renters and vehicle owners
- **🔐 Firebase Authentication** - Secure user management
- **📱 Responsive Design** - Works on all devices

### 🚀 Smart Features
- **🤖 AI-Powered Booking** - Smart suggestions for optimal pick-up/drop-off
- **⚖️ Dynamic Rebalancing** - Automatic fleet distribution
- **👫 Peer-to-Peer Returns** - Community-driven vehicle returns
- **🌐 Multi-Agency Network** - Cross-city vehicle returns
- **🎁 Incentive System** - Rewards for helping balance fleet
- **📊 Real-time Tracking** - Live vehicle availability

## 🎨 Screenshots

### Landing Page
- Beautiful hero section with compelling messaging
- Feature showcase with interactive cards
- Pricing section with transparent rates
- Call-to-action for both user types

### Dashboard
- Vehicle browsing with real-time availability
- Rental management and history
- Vehicle listing for owners
- Cost calculation and booking

## 🚀 Quick Start

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- Firebase account

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/harleen-kaur-02/fasto.git
   cd Fasto
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure Firebase**
   - Go to [Firebase Console](https://console.firebase.google.com/)
   - Create a new project
   - Enable Authentication (Email/Password)
   - Enable Firestore Database
   - Copy your config to `src/firebase.ts`

4. **Start the development server**
   ```bash
   npm start
   ```

5. **Open your browser**
   Navigate to `http://localhost:3000`

## 🔧 Configuration

### Firebase Setup

1. **Authentication**
   - Go to Authentication > Sign-in method
   - Enable Email/Password provider

2. **Firestore Database**
   - Go to Firestore Database
   - Create database in test mode
   - Set up security rules:

   ```javascript
   rules_version = '2';
   service cloud.firestore {
     match /databases/{database}/documents {
       match /vehicles/{document} {
         allow read, write: if request.auth != null;
       }
       match /rentals/{document} {
         allow read, write: if request.auth != null;
       }
     }
   }
   ```

## 💰 Pricing Structure

| Vehicle Type | Rate per Hour | Features |
|-------------|---------------|----------|
| **Scooter** | ₹25 | Perfect for city rides, easy parking |
| **Bike** | ₹40 | Great for longer rides, comfortable |
| **Premium Bike** | ₹60 | Latest models, enhanced safety |

## 🏗️ Project Structure

```
smart-rental-app/
├── public/
├── src/
│   ├── components/
│   │   ├── Auth.tsx          # Authentication component
│   │   ├── Dashboard.tsx     # Main dashboard
│   │   └── LandingPage.tsx   # Landing page
│   ├── contexts/
│   │   └── AuthContext.tsx   # Authentication context
│   ├── firebase.ts           # Firebase configuration
│   ├── App.tsx              # Main app component
│   └── index.css            # Global styles
├── README.md
├── SETUP.md
└── package.json
```

## 🛠️ Tech Stack

- **Frontend**: React 18, TypeScript
- **Styling**: Tailwind CSS
- **Backend**: Firebase (Authentication, Firestore)
- **State Management**: React Context
- **Build Tool**: Create React App

## 🚀 Deployment

### Vercel (Recommended)
1. Connect your GitHub repository to Vercel
2. Configure environment variables
3. Deploy automatically on push

### Netlify
1. Build the project: `npm run build`
2. Deploy the `build` folder to Netlify
3. Configure redirects for SPA routing

### Firebase Hosting
1. Install Firebase CLI: `npm install -g firebase-tools`
2. Login: `firebase login`
3. Initialize: `firebase init hosting`
4. Deploy: `firebase deploy`

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open a Pull Request


## 👨‍💻 Author

**Harleen Kaur**
- GitHub: [@harleen-kaur-02](https://github.com/harleen-kaur-02)]

## 🙏 Acknowledgments

- Firebase for backend services
- Tailwind CSS for beautiful styling
- React community for amazing tools
- Unsplash for vehicle images

## 📞 Support

If you have any questions or need help, please:
- Open an issue on GitHub


**Made with ❤️ for the future of vehicle rental**

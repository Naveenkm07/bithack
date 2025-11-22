# CodePlayzTrustPass - Advanced Digital Certificate Verification System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js](https://img.shields.io/badge/Node.js-18.x-green.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18.x-blue.svg)](https://reactjs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-7.x-green.svg)](https://www.mongodb.com/)

A cutting-edge digital certificate management and verification system that leverages SHA-256 cryptographic hashing for authenticity verification and is architected for future Zero-Knowledge Proof (ZKP) integration. Built with modern web technologies for a seamless user experience.

## 🌟 Key Features

### 🔐 Secure Certificate Management
- **Secure Upload**: Upload digital certificates in PDF, PNG, JPG, and JPEG formats
- **Cryptographic Hashing**: Automatic SHA-256 hash generation for tamper-proof verification
- **Metadata Storage**: Comprehensive certificate metadata stored in MongoDB with fallback to in-memory storage

### 📱 Modern User Interface
- **Dark/Light Theme**: Automatic system preference detection with manual toggle
- **Responsive Design**: Fully responsive interface that works on mobile, tablet, and desktop
- **Interactive Components**: Drag-and-drop file uploads, animated transitions, and intuitive navigation
- **Real-time Feedback**: Visual indicators and user-friendly error messages

### 🔍 Advanced Verification
- **QR Code Generation**: Scannable QR codes for instant certificate verification
- **Hash-based Verification**: Cryptographically secure verification using SHA-256 hashes
- **Certificate Details**: Comprehensive certificate information display with copy-to-clipboard functionality

### 🚀 Future-Ready Architecture
- **Zero-Knowledge Proof Ready**: Pre-architected for ZKP integration for privacy-preserving verification
- **Scalable Design**: Modular architecture that supports future enhancements
- **API-first Approach**: RESTful API design for easy integration with other systems

## 🏗️ System Architecture

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   Frontend      │    │     API          │    │   Database      │
│   (React/Vite)  │◄──►│   (Express.js)   │◄──►│   (MongoDB)     │
└─────────────────┘    └──────────────────┘    └─────────────────┘
```

## 🚀 Quick Start

### Prerequisites
- Node.js (v18 or higher)
- MongoDB (v4.4 or higher)
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Naveenkm07/bithack.git
   cd bithack
   ```

2. **Start MongoDB**
   Ensure MongoDB is running on your system:
   ```bash
   mongod
   ```

3. **Backend Setup**
   ```bash
   cd FileSave-hash-MetaData-main/apps/api
   npm install
   npm start
   ```
   The API will be available at `http://localhost:5000`

4. **Frontend Setup**
   ```bash
   cd FileSave-hash-MetaData-main/apps/web
   npm install
   npm run dev
   ```
   The web application will be available at `http://localhost:5173`

### Environment Variables

#### API (.env)
```env
PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/trustpass
JWT_SECRET=supersecretkey123
```

## 🛠️ API Endpoints

### Authentication
- `POST /auth/register` - Register a new user
- `POST /auth/login` - Login with existing credentials

### Certificate Management
- `POST /certificates/upload` - Upload a certificate
- `GET /certificates/:id` - Retrieve certificate details by ID

## 🧰 Technology Stack

### Backend
- **Node.js** with Express.js
- **MongoDB** with Mongoose
- **Multer** for file uploads
- **Crypto** for SHA-256 hashing
- **JWT** for authentication
- **BCrypt** for password hashing
- **CORS** for cross-origin requests

### Frontend
- **React** with Vite
- **Tailwind CSS** for styling
- **React Router** for navigation
- **Axios** for API requests
- **QRCode.react** for QR code generation
- **Headless UI** for accessible UI components

## 🔄 Workflow

1. **Upload Certificate**: User uploads a digital certificate through the web interface
2. **Hash Generation**: Backend automatically generates a SHA-256 hash of the file
3. **Metadata Storage**: Certificate metadata (filename, hash, path, timestamp) stored in MongoDB
4. **Verification Ready**: User receives a unique certificate ID for future verification
5. **Zero-Knowledge Proofs**: (Future) Generate and verify ZKPs for privacy-preserving authentication

## 🎨 UI Features

### Dashboard
- Interactive statistics cards with animated counters
- Feature navigation cards with hover effects
- Visual workflow explanation with connecting elements
- Dark/light theme toggle with system preference detection

### Certificate Upload
- Drag-and-drop file upload area
- File size formatting and validation
- Upload progress tracking
- Visual feedback for all actions

### Certificate Details
- Comprehensive certificate information display
- QR code generation for easy sharing
- Copy-to-clipboard functionality with visual feedback
- Download certificate option

### Zero-Knowledge Proof
- Proof generation interface
- Proof verification system
- Detailed explanation of ZKP technology

## 🌋 Future Enhancements

- **Zero-Knowledge Proof Integration**: Full ZKP implementation for privacy-preserving verification
- **IPFS Integration**: Decentralized certificate storage using IPFS
- **Advanced Metadata Extraction**: AI-powered certificate metadata extraction
- **Multi-signature Support**: Support for multi-signature certificates
- **Blockchain Integration**: Immutable certificate records on blockchain
- **Mobile App**: Native mobile applications for iOS and Android

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Naveen Kumar K M** - *Initial work* - [Naveenkm07](https://github.com/Naveenkm07)

## 🙏 Acknowledgments

- Thanks to all contributors who have helped shape this project
- Inspired by the need for secure digital certificate verification in the modern world
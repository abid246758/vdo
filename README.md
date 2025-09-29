# Secure Video Chat Application

A modern, secure video chat application with end-to-end encryption, built with React and Node.js.

## 🚀 Features

- **End-to-End Encryption**: All communications are encrypted using AES-256-CBC
- **Modern UI**: Beautiful, responsive interface built with Material-UI
- **Real-time Communication**: WebRTC for peer-to-peer video calls
- **Room-based Calls**: Create or join rooms for group video calls
- **Screen Sharing**: Share your screen during calls
- **Security**: Rate limiting, CORS protection, and helmet security headers
- **Responsive Design**: Works on desktop and mobile devices

## 🏗️ Architecture

### Project Structure
```
project_video_chat-master/
├── backend/                 # Backend server
│   ├── server.js           # Main server file
│   ├── config.js           # Configuration
│   ├── package.json        # Backend dependencies
│   └── node_modules/       # Backend packages
├── frontend/               # Frontend application
│   ├── src/
│   │   ├── pages/          # React pages
│   │   ├── contexts/       # React contexts
│   │   └── App.js          # Main app component
│   ├── public/             # Static files
│   ├── package.json        # Frontend dependencies
│   └── node_modules/       # Frontend packages
├── start.sh               # Startup script (macOS/Linux)
├── start.bat              # Startup script (Windows)
└── README.md              # This file
```

### Backend (`/backend`)
- **Express.js** server with Socket.io for real-time communication
- **Security middleware** (Helmet, CORS, Rate limiting)
- **End-to-end encryption** for all signaling data
- **Room management** with encryption key generation
- **Health monitoring** and connection tracking

### Frontend (`/frontend`)
- **React 18** with modern hooks and context
- **Material-UI v5** for beautiful, responsive components
- **React Router** for navigation
- **Crypto-JS** for client-side encryption
- **Socket.io Client** for real-time communication

## 🛠️ Installation & Setup

### Prerequisites
- Node.js 16+ 
- npm or yarn

### Backend Setup

```bash
# Navigate to backend directory
cd backend

# Install dependencies
npm install

# Create environment file
cp .env.example .env

# Start development server
npm run dev

# Or start production server
npm start
```

### Frontend Setup

```bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Start development server
npm start
```

## 🔧 Configuration

### Backend Environment Variables

Create a `.env` file in the backend directory:

```env
PORT=4001
NODE_ENV=development
JWT_SECRET=your-super-secret-jwt-key-here
ENCRYPTION_KEY=your-32-character-encryption-key
ALLOWED_ORIGINS=http://localhost:3000,http://localhost:3001
```

### Frontend Environment Variables

Create a `.env` file in the frontend directory:

```env
REACT_APP_SERVER_URL=http://localhost:4001
```

## 🚀 Running the Application

### Quick Start (Recommended)

**For macOS/Linux:**
```bash
./start.sh
```

**For Windows:**
```batch
start.bat
```

### Manual Start

1. **Start the backend server:**
   ```bash
   cd backend
   npm start
   ```

2. **Start the frontend application:**
   ```bash
   cd frontend
   npm start
   ```

3. **Open your browser:**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:4001

## 🔒 Security Features

- **End-to-End Encryption**: All signaling data is encrypted using AES-256-CBC
- **Rate Limiting**: Prevents abuse with configurable rate limits
- **CORS Protection**: Configured for specific origins
- **Helmet Security**: Security headers for protection against common vulnerabilities
- **Input Validation**: All inputs are validated and sanitized
- **Connection Authentication**: Socket connections require authentication tokens

## 📱 Usage

1. **Create a Room**: Enter your name and click "Create Room"
2. **Join a Room**: Enter your name and room ID to join an existing room
3. **Share Room**: Use the share button to copy the room link
4. **Video Controls**: Mute/unmute, turn video on/off, screen share
5. **End Call**: Click the red phone button to end the call

## 🧪 Testing

### Backend Tests
```bash
cd backend
npm test
```

### Frontend Tests
```bash
cd frontend
npm test
```

## 📦 Production Deployment

### Backend Deployment
1. Set `NODE_ENV=production`
2. Configure SSL certificates
3. Set up proper environment variables
4. Use a process manager like PM2

### Frontend Deployment
1. Build the application: `npm run build`
2. Serve the build folder with a web server
3. Configure environment variables for production

## 🔧 API Endpoints

- `GET /health` - Health check endpoint
- `GET /api/rooms` - Get active rooms
- `GET /api/connections` - Get active connections

## 🐛 Troubleshooting

### Common Issues

1. **Connection Refused**: Ensure both backend and frontend are running
2. **Camera/Microphone Access**: Check browser permissions
3. **Encryption Errors**: Verify room keys are properly generated
4. **Port Conflicts**: Change ports in configuration if needed

### Browser Compatibility

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## 📄 License

MIT License - see LICENSE file for details

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests
5. Submit a pull request

## 📞 Support

For support and questions, please open an issue on GitHub.
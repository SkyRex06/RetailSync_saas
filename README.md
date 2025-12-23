# RetailSync SaaS

![RetailSync Logo](https://via.placeholder.com/150x50?text=RetailSync) <!-- Replace with actual logo -->

RetailSync is a revolutionary SaaS platform that leverages multi-agent AI technology to optimize retail inventory management. By creating a collaborative ecosystem between stores, warehouses, suppliers, and customers, RetailSync eliminates stockouts, reduces excess inventory, and maximizes profitability through intelligent data synchronization and predictive analytics.

## 🚀 Features

### Core Capabilities
- **Multi-Agent AI Architecture**: Intelligent agents collaborate across the retail ecosystem
- **Real-time Inventory Synchronization**: Seamless data sync between multiple systems
- **Advanced Demand Forecasting**: AI-powered predictions to optimize stock levels
- **Google Sheets Integration**: Easy data import/export and management
- **Automated Replenishment**: Smart ordering suggestions based on historical data
- **Performance Analytics**: Comprehensive dashboards and ROI tracking
- **Webhook Support**: Real-time notifications and integrations
- **Multi-tenant Architecture**: Secure, isolated environments for each client

### AI-Powered Insights
- Stock efficiency optimization (up to 94.3%)
- Demand pattern recognition
- Supplier performance analysis
- Customer behavior prediction
- Seasonal trend analysis
- Waste reduction algorithms

## 🛠 Tech Stack

### Frontend
- **React 18** with TypeScript
- **Vite** for fast development and building
- **Tailwind CSS** for styling
- **Shadcn/ui** component library
- **React Router** for navigation
- **Firebase** for authentication and real-time features
- **Google Generative AI** for chat functionality

### Backend
- **Node.js** with Express.js
- **Passport.js** for Google OAuth authentication
- **Google APIs** (Sheets, Drive) for data integration
- **Express Handlebars** for server-side rendering
- **Multer** for file uploads
- **Axios** for HTTP requests

### Infrastructure
- **RESTful API** design
- **Session-based authentication**
- **Environment-based configuration**
- **CORS enabled**
- **Webhook endpoints**

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- **Node.js** (v18 or higher)
- **npm** or **bun** package manager
- **Google Cloud Console** account for API credentials
- **Firebase** project for frontend authentication

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/SkyRex06/RetailSync_saas.git
   cd RetailSync_saas
   ```

2. **Install frontend dependencies**
   ```bash
   npm install
   # or
   bun install
   ```

3. **Install backend dependencies**
   ```bash
   cd backend
   npm install
   cd ..
   ```

## ⚙️ Configuration


### Google Cloud Setup

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project or select existing one
3. Enable Google Sheets API and Google Drive API
4. Create OAuth 2.0 credentials
5. Add authorized redirect URIs:
   - `http://localhost:3000/auth/google/callback`
6. Copy Client ID and Client Secret to backend/.env

### Firebase Setup

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Create a new project
3. Enable Authentication and Firestore
4. Go to Project Settings > General > Your apps
5. Add a web app and copy the config to frontend/.env

## 🚀 Running the Application

### Development Mode

1. **Start the backend server**
   ```bash
   cd backend
   npm start
   # or
   node src/server.js
   ```
   Backend will run on http://localhost:3000

2. **Start the frontend development server**
   ```bash
   npm run dev
   ```
   Frontend will run on http://localhost:8080

3. **Access the application**
   - Open http://localhost:8080 in your browser
   - The backend API is available at http://localhost:3000

### Production Build

1. **Build the frontend**
   ```bash
   npm run build
   ```

2. **Start production server**
   ```bash
   npm run preview
   ```

## 📡 API Endpoints

### Authentication
- `GET /auth/google` - Initiate Google OAuth
- `GET /auth/google/callback` - OAuth callback
- `GET /auth/logout` - Logout user

### Sheets Operations
- `POST /api/sheets/copy` - Copy a Google Sheet
- `POST /api/sheets/upload` - Upload spreadsheet file
- `GET /api/sheets/list` - List user's sheets
- `POST /api/sheets/create` - Create new sheet

### Webhooks
- `POST /webhook/data` - Receive data updates
- `GET /webhook/status` - Check webhook status

### Static Routes
- `GET /` - Main application page

## 🏗 Project Structure

```
RetailSyncSaaS/
├── backend/                    # Node.js backend
│   ├── src/
│   │   ├── config/
│   │   │   └── passport-setup.js
│   │   ├── controllers/
│   │   │   ├── authController.js
│   │   │   ├── sheetController.js
│   │   │   └── webhookController.js
│   │   ├── routes/
│   │   │   ├── apiRoutes.js
│   │   │   ├── authRoutes.js
│   │   │   └── webhookRoutes.js
│   │   ├── services/
│   │   │   └── googleService.js
│   │   ├── views/
│   │   │   └── index.html
│   │   └── server.js
│   ├── package.json
│   └── .env
├── src/                        # React frontend
│   ├── components/
│   │   ├── ui/                 # Shadcn/ui components
│   │   ├── chat/               # Chat widget
│   │   ├── HeroSection.tsx
│   │   ├── FeaturesSection.tsx
│   │   └── ...
│   ├── pages/
│   │   ├── Index.tsx
│   │   ├── FeaturesPage.tsx
│   │   ├── PricingPage.tsx
│   │   └── ...
│   ├── context/
│   │   └── ChatContext.tsx
│   ├── data/
│   │   └── pricing.ts
│   ├── hooks/
│   ├── lib/
│   │   ├── firebase.ts
│   │   ├── gemini.ts
│   │   └── utils.ts
│   └── main.tsx
├── public/                     # Static assets
├── package.json
├── vite.config.ts
├── tailwind.config.ts
└── .env
```

## 🔄 How It Works

1. **User Authentication**: Users authenticate via Google OAuth
2. **Data Integration**: Connect Google Sheets for inventory data
3. **AI Processing**: Multi-agent system analyzes data patterns
4. **Optimization**: Generate recommendations for inventory management
5. **Real-time Sync**: Automated updates across all connected systems
6. **Reporting**: Comprehensive analytics and performance metrics

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow TypeScript best practices
- Use ESLint configuration
- Write meaningful commit messages
- Test your changes thoroughly
- Update documentation as needed


## 🗺 Roadmap

- [ ] Mobile app development
- [ ] Advanced ML models for forecasting
- [ ] Integration with major POS systems
- [ ] Real-time collaboration features
- [ ] API marketplace for third-party integrations

---

**Built with ❤️ for the retail industry**
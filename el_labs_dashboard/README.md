# ElevenLabs AI Call Agent Dashboard

A comprehensive dashboard for monitoring and analyzing AI call agent performance using ElevenLabs Conversational AI, complete with real-time metrics, customer feedback analysis, and automated reporting.

## 🚀 Features

- **Real-time Call Analytics**: Monitor total calls, success rates, and call durations
- **Booking Management**: Track appointment bookings generated through AI calls
- **Customer Feedback Analysis**: AI-powered sentiment analysis using OpenAI
- **ElevenLabs Credits Monitoring**: Track API usage and remaining credits
- **Automated PDF Reports**: Generate comprehensive performance reports
- **Interactive Charts**: Visual representation of trends and metrics
- **Modern UI**: Clean, responsive dashboard with Material-UI components

## 📋 Prerequisites

Before setting up the project, ensure you have:

- **Node.js** (version 16.0.0 or higher)
- **npm** or **yarn** package manager
- **ElevenLabs API Key** (for call analytics and voice services)
- **OpenAI API Key** (for customer feedback sentiment analysis)

## 🛠️ Initial Setup

### 1. Clone and Install Dependencies

```bash
# Clone the repository
git clone <repository-url>
cd el_labs_dashboard

# Install dependencies
npm install
# or if you prefer yarn
yarn install
```

### 2. Environment Variables Setup

Create a `.env.local` file in the root directory and add the following environment variables:

```env
# ElevenLabs API Configuration
ELEVENLABS_API_KEY=your_elevenlabs_api_key_here

# OpenAI API Configuration (for feedback analysis)
OPENAI_API_KEY=your_openai_api_key_here
```

**⚠️ Important**: 
- Never commit `.env.local` files to version control
- Obtain your ElevenLabs API key from: https://elevenlabs.io/app/speech-synthesis
- Obtain your OpenAI API key from: https://platform.openai.com/api-keys

### 3. Run the Development Server

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser. The application will automatically redirect you to the dashboard at `/dashboard`.

## 🏗️ Build and Deploy

### For Production Build

```bash
# Create production build
npm run build

# Start production server
npm start
```

### For Linting

```bash
npm run lint
```

## 🔧 Environment Variables Reference

| Variable | Required | Description | Example |
|----------|----------|-------------|---------|
| `ELEVENLABS_API_KEY` | ✅ Yes | API key for ElevenLabs services | `sk-...` |
| `OPENAI_API_KEY` | ⚠️ Optional | API key for OpenAI (fallback sentiment analysis used if not provided) | `sk-...` |

## 📊 Dashboard Features

### Analytics Tracked
- **Total Calls**: Complete call volume from ElevenLabs
- **Success Rate**: Percentage of successful vs. unsuccessful calls
- **Booking Conversions**: Appointments scheduled through AI calls
- **Customer Satisfaction**: AI-analyzed feedback sentiment (1-5 scale)
- **Credit Usage**: Real-time ElevenLabs API credit consumption

### API Integrations
- **ElevenLabs Conversational AI**: Call data and credit monitoring
- **GHL (GoHighLevel)**: Booking and form submission tracking
- **OpenAI GPT**: Advanced sentiment analysis for customer feedback

## 🔗 API Endpoints

- `/api/gettotalcalls` - Fetch ElevenLabs conversation data
- `/api/getElevenLabsUsage` - Monitor credit usage
- `/api/getbookingsnumber` - Track booking conversions
- `/api/getfeedback` - Analyze customer feedback
- `/api/generateReport` - Create PDF reports

## 🎯 Navigation

The application automatically redirects from the root URL (`/`) to `/dashboard` for immediate access to the main interface.

## 🛠️ Technology Stack

- **Frontend**: React 19, Next.js 15.3.2
- **Styling**: Material-UI, CSS Modules
- **Charts**: Chart.js, Recharts
- **PDF Generation**: PDFKit
- **HTTP Client**: Axios
- **Icons**: Lucide React

## 📁 Project Structure

```
el_labs_dashboard/
├── components/          # Reusable React components
│   ├── dashboard/      # Dashboard-specific components
│   └── DashboardStats.js
├── pages/              # Next.js pages and API routes
│   ├── api/           # Backend API endpoints
│   ├── dashboard/     # Main dashboard page
│   └── index.js       # Root redirect to dashboard
├── public/            # Static assets and generated reports
├── styles/            # CSS modules and global styles
└── README.md          # Project documentation
```

## 🚨 Troubleshooting

### Common Issues

1. **API Key Errors**: Ensure all required environment variables are set in `.env.local`
2. **Build Failures**: Clear `.next` folder and reinstall dependencies
3. **Port Conflicts**: Change the port with `npm run dev -- -p 3001`

### Support

For technical issues or feature requests, please check the project documentation or contact the development team.

## 📈 Performance Monitoring

The dashboard includes built-in performance monitoring for:
- API response times
- Credit usage optimization
- Call success rate trending
- Customer satisfaction metrics

---

**Note**: This dashboard requires active ElevenLabs and OpenAI accounts with valid API keys for full functionality.

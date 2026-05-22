# DropAI Platform - AI Dropshipping Command Center

A complete, runnable AI-powered dropshipping platform with real backend API, database, and interactive frontend.

## 🚀 Quick Start

### Local Development

```bash
# Install dependencies
pip install -r requirements.txt

# Run locally
bash start.sh  # Linux/Mac
start.bat      # Windows
```

Open http://localhost:5000

## ⭐ Features

### AI Research Agent
- **Autonomous Product Discovery**: Scans TikTok, Reddit, Google Trends, Instagram, YouTube
- **Viral Scoring Algorithm**: Rates products 0-100 based on trend data
- **Profit Calculator**: Automatic margin analysis
- **Real-time Progress**: Watch the AI research in action with live updates

### Multi-Platform Integration
- **Amazon Seller Central** - OAuth connection flow
- **eBay Developer API** - OAuth connection flow  
- **Shopify Admin API** - Store connection
- **Etsy API** - OAuth connection flow
- **One-click bulk listing** across all connected platforms
- **Real connection simulation** with API logging

### Supplier Network
- 6 pre-loaded suppliers with reliability ratings
- Auto-matching based on product category
- Shipping time and order volume tracking

### AI Tools
- **Description Writer**: SEO-optimized product descriptions
- **Price Optimizer**: Dynamic pricing with competitor analysis
- **API Logs**: Real-time backend API logging

### Analytics Dashboard
- Revenue charts with Chart.js
- Platform breakdown
- Daily trend tracking
- 30 days of seeded analytics data

## 🏗️ Architecture

```
Dropai-platform/
├── backend/
│   └── app.py              # Flask API server (all endpoints)
├── frontend/
│   └── index.html          # Complete SPA with API integration
├── requirements.txt        # Python dependencies
├── Dockerfile              # Container configuration
├── docker-compose.yml      # Docker Compose setup
├── Procfile                # Heroku deployment
├── vercel.json             # Vercel configuration
├── netlify.toml            # Netlify configuration
├── DEPLOYMENT.md           # Detailed deployment guide
└── start.sh/start.bat      # Launch scripts
```

## 💡 API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/research/start` | POST | Start AI product research |
| `/api/research/status/<id>` | GET | Check research progress |
| `/api/products` | GET | Get discovered products |
| `/api/platforms` | GET | List platform connections |
| `/api/platforms/<name>/connect` | POST | Initiate OAuth flow |
| `/api/platforms/<name>/disconnect` | POST | Disconnect platform |
| `/api/listings/bulk` | POST | Bulk list to platforms |
| `/api/suppliers` | GET | List suppliers |
| `/api/analytics/dashboard` | GET | Dashboard stats |
| `/api/ai/generate-description` | POST | AI product descriptions |
| `/api/ai/optimize-price` | POST | AI price optimization |

## 🚀 Deployment

### Heroku

```bash
heroku login
heroku create your-dropai-app
heroku config:set FLASK_ENV=production
git push heroku main
heroku open
```

### Vercel

1. Connect GitHub repo to Vercel
2. Vercel will auto-detect configuration
3. Deploy instantly

### Netlify

1. Connect GitHub repo to Netlify
2. Build command: `pip install -r requirements.txt`
3. Functions directory: `backend`

### Docker

```bash
docker build -t dropai-platform .
docker run -p 5000:5000 dropai-platform
docker-compose up
```

## 📊 Using the Platform

### 1. Connect Your Stores
- Click on any platform card (Amazon, eBay, Shopify, Etsy)
- Click "Connect" button
- The platform turns green when connected

### 2. Run AI Research
- Click "Start AI Research"
- Watch the progress bar as the agent scans trends
- Products appear automatically when research completes

### 3. Select & List Products
- Click products to select them (checkmark appears)
- Click "List to Selected Platforms" to bulk publish
- Results show in a modal with listing IDs

### 4. Use AI Tools
- **Description Writer**: Enter product name + keywords
- **Price Optimizer**: Enter cost + competitor prices
- **API Logs**: See all backend API calls in real-time

### 5. View Analytics
- Revenue chart updates automatically
- See platform performance breakdown
- Track daily trends

## 📝 Database

SQLite database (`dropai.db`) is auto-created with:
- Products table
- Listings table  
- Platform connections table
- Suppliers table
- Analytics table
- Research jobs table

## 🔧 Tech Stack

- **Backend**: Python 3, Flask, SQLite, Threading
- **Frontend**: Vanilla JS, Tailwind CSS, Chart.js, Axios
- **Deployment**: Docker, GitHub Actions, Heroku, Vercel, Netlify
- **CI/CD**: GitHub Actions workflows

## 🔐 Production Setup

Update credentials in `.env` for real platform integration

## 📝 License

MIT License - Built for dropshipping automation.

## 🤝 Contributing

Feel free to fork and submit pull requests!

## 📧 Support

For issues and questions, open a GitHub issue.

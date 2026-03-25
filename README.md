> ⚠️ This repo is a starting point, not a solution. 
> You will get stuck. That's the point. Google is your best friend.

# URL Shortener with Analytics

> Shorten any URL and track every click with location, device and referrer data.

## What You Will Learn
- How URL shortening actually works with redirects
- How to track and store analytics data
- How to build a dashboard to visualize data
- How to work with MongoDB for document storage

## Tech Stack
- Node.js
- Express
- MongoDB
- React
- Recharts
- Vercel (frontend)
- Railway (backend)

## Getting Started

### Prerequisites
- Node.js 18+ installed
- MongoDB installed locally or a free MongoDB Atlas account

### Installation
```bash
# Backend
git clone https://github.com/thanos.zip/url-shortener
cd url-shortener/backend
npm install
cp .env.example .env
npm run dev

# Frontend
cd ../frontend
npm install
npm run dev
```

## Project Structure
```
url-shortener/
├── backend/
│   ├── index.js                   # Server entry point
│   ├── routes/
│   │   ├── shorten.js             # URL shortening routes here
│   │   └── analytics.js          # Analytics routes here
│   ├── controllers/
│   │   ├── shortenController.js   # Shortening logic here
│   │   └── analyticsController.js # Analytics logic here
│   ├── models/
│   │   ├── url.js                 # URL schema here
│   │   └── click.js              # Click event schema here
│   └── .env.example
├── frontend/
│   ├── src/
│   │   ├── App.jsx
│   │   └── components/
│   │       ├── Shorten.jsx        # Input and result UI here
│   │       └── Dashboard.jsx     # Analytics charts here
│   └── package.json
└── README.md
```

## What To Build
- POST /shorten — generate a unique short code and save the original URL
- GET /:code — look up the short code, log the click event, redirect to original URL
- Store click data — timestamp, user agent, referrer
- GET /analytics/:code — return all click data for a short URL
- Build a React dashboard showing total clicks and clicks over time with Recharts
- Deploy backend on Railway, frontend on Vercel

## Stretch Goals
- Add custom short codes — let users choose their own alias
- Add expiry dates — links that stop working after a set time
- Add QR code generation for each short URL

## Resources
- https://mongoosejs.com/docs/
- https://recharts.org/en-US/guide
- https://railway.app/docs

---
Built for [@thanos.zip](https://instagram.com/thanos.zip) followers.

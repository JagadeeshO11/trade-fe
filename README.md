# Trade Nexus - Full Stack Trading Advisory Platform

## Project Structure
```
p2/
├── backend/          # Node.js + Express API
│   ├── routes/
│   │   ├── payment.js    # Razorpay payment endpoints
│   │   └── contact.js    # Contact form endpoint
│   ├── server.js
│   └── .env
└── frontend/         # React App
    └── src/
        ├── components/
        │   ├── Navbar.js
        │   ├── Hero.js
        │   ├── About.js
        │   ├── Services.js
        │   ├── TrackRecord.js
        │   ├── Plans.js
        │   ├── PaymentModal.js
        │   ├── WhyUs.js
        │   ├── Disclaimer.js
        │   └── Footer.js
        ├── App.js
        └── App.css
```

## Setup Instructions

### 1. Backend Setup
```bash
cd backend
# Edit .env with your credentials:
#   RAZORPAY_KEY_ID=your_key_id
#   RAZORPAY_KEY_SECRET=your_key_secret
#   EMAIL_USER=your_gmail
#   EMAIL_PASS=your_app_password
npm run dev
```

### 2. Frontend Setup
```bash
cd frontend
# Edit .env:
#   REACT_APP_API_URL=http://localhost:5000/api
#   REACT_APP_RAZORPAY_KEY_ID=your_key_id
npm start
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/health | Health check |
| GET | /api/payment/plans | Get all subscription plans |
| POST | /api/payment/create-order | Create Razorpay order |
| POST | /api/payment/verify | Verify payment signature |
| POST | /api/contact | Submit contact/lead form |

## Razorpay Integration
1. Sign up at https://razorpay.com
2. Get Key ID and Key Secret from Dashboard > Settings > API Keys
3. Add them to `backend/.env` and `frontend/.env`

## Gmail App Password (for contact emails)
1. Enable 2FA on your Google account
2. Go to Google Account > Security > App Passwords
3. Generate a password for "Mail" and use it as EMAIL_PASS

## Company Info
- **Name:** Trade Nexus
- **SEBI Reg:** INH200008024
- **Address:** HSR Layout, 7th Sector, Near 5th Main Road, Bangalore - 560102
- **Contact:** 70900-38951 / 84970-77442

# 🚀 Vercel Deployment Guide

## Deploy Frontend + Backend Together (5 minutes)

### Step 1: Setup Railway Database (2 minutes)
1. Go to https://railway.app
2. Sign up with GitHub
3. "Start a New Project" → "Provision PostgreSQL"
4. Click PostgreSQL service → Variables tab → Copy `DATABASE_URL`

### Step 2: Deploy to Vercel (2 minutes)
1. Go to https://vercel.com
2. Login with GitHub
3. "New Project" → Import `Nirmit210/pulsepixeltech`
4. Keep root directory as default
5. Click "Deploy"

### Step 3: Add Environment Variables (1 minute)
After deployment, go to Settings → Environment Variables:

```
NODE_ENV=production
DATABASE_URL=paste_your_railway_database_url_here
JWT_SECRET=pulsepixeltech_super_secret_jwt_key_for_production_make_it_very_long_and_secure_2024
SAMBANOVA_API_KEY=1c0e0109-1ee0-456a-8470-ae17fa1643e6
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_gmail_app_password
PAYMENT_SIMULATION_DELAY=1000
PAYMENT_SUCCESS_RATE=98
MAX_FILE_SIZE=5242880
UPLOAD_PATH=./uploads
FRONTEND_URL=https://your-vercel-app.vercel.app
NEXT_PUBLIC_API_URL=https://your-vercel-app.vercel.app
NEXT_PUBLIC_APP_NAME=PulsePixelTech
NEXT_PUBLIC_APP_URL=https://your-vercel-app.vercel.app
```

### Step 4: Redeploy
1. Go to Deployments tab
2. Click "Redeploy" on latest deployment

## 🎉 Done!
Your app is live at: `https://your-app.vercel.app`

## 🧪 Test
- Homepage should load with categories
- `/api/health` should return "OK"
- Chatbot should respond with AI
- Login/register should work

## 💰 Cost
- **Vercel**: Free (hosting)
- **Railway**: Free (1GB PostgreSQL)
- **Total**: $0

## 🆘 Issues?
- Check Vercel function logs
- Verify all environment variables are set
- Ensure Railway database is running
# 🚀 Vercel Deployment Guide

## Deploy Frontend + Backend Together (5 minutes)

### Step 1: Setup Free PostgreSQL Database (2 minutes)

**Option A: Aiven (Recommended - 1 month free)**
1. Go to https://aiven.io
2. Sign up with GitHub
3. Create PostgreSQL service
4. Copy connection string from service overview

**Option B: ElephantSQL (20MB free)**
1. Go to https://www.elephantsql.com
2. Sign up with GitHub
3. Create new instance (Tiny Turtle - Free)
4. Copy connection string

**Option C: Render (90 days free)**
1. Go to https://render.com
2. Sign up with GitHub
3. Create PostgreSQL database
4. Copy connection string

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
DATABASE_URL=paste_your_database_connection_string_here
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
- **Database**: Free (Aiven/ElephantSQL/Render)
- **Total**: $0

## 🆘 Issues?
- Check Vercel function logs
- Verify all environment variables are set
- Ensure database connection string is correct
- Test database connectivity

## 🔗 Database Providers
- **Aiven**: https://aiven.io (1 month free, then $19/month)
- **ElephantSQL**: https://elephantsql.com (20MB free forever)
- **Render**: https://render.com (90 days free, then $7/month)
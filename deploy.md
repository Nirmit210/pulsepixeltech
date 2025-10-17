# 🚀 One-Click Deployment Guide

## Quick Deploy to Vercel (5 minutes)

### Step 1: Go to Vercel
1. Open: https://vercel.com
2. Click "Sign up" or "Login"
3. Choose "Continue with GitHub"
4. Authorize Vercel to access your GitHub

### Step 2: Import Your Project
1. Click "New Project" (big button)
2. Find "Nirmit210/pulsepixeltech" in the list
3. Click "Import" next to it

### Step 3: Deploy Backend First
1. **Root Directory**: Select `backend`
2. **Framework Preset**: Other
3. **Build Command**: `npm run build`
4. **Output Directory**: (leave empty)
5. Click "Deploy"

### Step 4: Add Backend Environment Variables
After backend deploys, go to Settings → Environment Variables and add:

```
NODE_ENV=production
DATABASE_URL=postgresql://postgres:password@localhost:5432/pulsepixeltech
JWT_SECRET=your_super_secret_jwt_key_here_make_it_very_long_and_secure_for_production
SAMBANOVA_API_KEY=1c0e0109-1ee0-456a-8470-ae17fa1643e6
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password
FRONTEND_URL=https://your-frontend-will-be-here.vercel.app
```

### Step 5: Deploy Frontend
1. Go back to Vercel dashboard
2. Click "New Project" again
3. Import "Nirmit210/pulsepixeltech" again
4. **Root Directory**: Select `frontend`
5. **Framework Preset**: Next.js
6. Click "Deploy"

### Step 6: Add Frontend Environment Variables
After frontend deploys, add these variables:

```
NEXT_PUBLIC_API_URL=https://your-backend-url.vercel.app
NEXT_PUBLIC_APP_NAME=PulsePixelTech
NEXT_PUBLIC_APP_URL=https://your-frontend-url.vercel.app
```

### Step 7: Update URLs
1. Copy your backend URL from Vercel
2. Update NEXT_PUBLIC_API_URL in frontend settings
3. Copy your frontend URL
4. Update FRONTEND_URL in backend settings
5. Redeploy both (click "Redeploy" in each project)

## 🎉 Done!
Your e-commerce platform will be live!

## Need Database?
Use Railway (free):
1. Go to railway.app
2. Create new project → PostgreSQL
3. Copy connection string from Variables
4. Use as DATABASE_URL in backend settings

**More Options**: See [FREE_DATABASE_OPTIONS.md](./FREE_DATABASE_OPTIONS.md) for alternatives
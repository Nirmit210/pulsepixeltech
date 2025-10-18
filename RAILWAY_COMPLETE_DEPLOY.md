# 🚂 Complete Railway Deployment Guide

## 🎯 Deploy Frontend + Backend + Database on Railway

### Step 1: Setup Services in Railway

You should have these 3 services in your Railway project:
1. **PostgreSQL** (database)
2. **pulsepixeltech-backend** (API)
3. **pulsepixeltech-frontend** (website)

### Step 2: Configure PostgreSQL Database

1. **Click on PostgreSQL service**
2. **Go to "Variables" tab**
3. **Copy the `DATABASE_URL`** value
4. **Save it** - you'll need this for backend configuration

### Step 3: Configure Backend Service

1. **Click on `pulsepixeltech-backend`**
2. **Go to "Settings" tab**:
   - **Root Directory**: `backend`
   - **Start Command**: `npm start`
3. **Go to "Variables" tab** and add:

```
NODE_ENV=production
DATABASE_URL=paste_your_postgresql_database_url_here
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
PORT=5000
```

### Step 4: Configure Frontend Service

1. **Click on `pulsepixeltech-frontend`**
2. **Go to "Settings" tab**:
   - **Root Directory**: `frontend`
   - **Build Command**: `npm run build`
   - **Start Command**: `npm start`
3. **Go to "Variables" tab** and add:

```
NODE_ENV=production
NEXT_PUBLIC_APP_NAME=PulsePixelTech
```

### Step 5: Get Service URLs

After deployment:

1. **Backend URL**:
   - Click on `pulsepixeltech-backend`
   - Go to "Settings" tab
   - Copy the domain (e.g., `pulsepixeltech-backend-production.up.railway.app`)

2. **Frontend URL**:
   - Click on `pulsepixeltech-frontend`
   - Go to "Settings" tab
   - Copy the domain (e.g., `pulsepixeltech-frontend-production.up.railway.app`)

### Step 6: Connect Services

**Update Frontend Variables:**
```
NEXT_PUBLIC_API_URL=https://your-backend-domain.up.railway.app
NEXT_PUBLIC_APP_URL=https://your-frontend-domain.up.railway.app
```

**Update Backend Variables:**
```
FRONTEND_URL=https://your-frontend-domain.up.railway.app
```

### Step 7: Deploy

1. **Deploy Backend**: Click "Deploy Now" in backend service
2. **Deploy Frontend**: Click "Deploy Now" in frontend service
3. **Wait for completion** (2-3 minutes each)

## 🎉 Success!

Your complete e-commerce platform will be live at:
- **Website**: `https://your-frontend-domain.up.railway.app`
- **API**: `https://your-backend-domain.up.railway.app`
- **Database**: Internal Railway PostgreSQL

## 🧪 Test Your Deployment

- [ ] **Homepage loads** with categories and products
- [ ] **API Health**: Visit `/api/health` - should return "OK"
- [ ] **Categories**: Visit `/categories` - should show categories
- [ ] **Chatbot**: Click chat button - should respond with AI
- [ ] **Login/Register**: Should work with demo accounts
- [ ] **Admin Dashboard**: Should be accessible

## 💰 Railway Pricing

**Free Tier Includes:**
- ✅ 500 hours/month execution time
- ✅ 1GB RAM per service
- ✅ 1GB PostgreSQL storage
- ✅ Custom domains
- ✅ Automatic deployments

**Perfect for development and small production apps!**

## 🔧 Troubleshooting

**Build Fails:**
- Check Railway logs in "Deployments" tab
- Verify root directory is set correctly
- Ensure all environment variables are set

**Database Connection Issues:**
- Verify DATABASE_URL is correct
- Check PostgreSQL service is running
- Ensure internal networking is working

**Frontend/Backend Not Connecting:**
- Verify API URLs are correct
- Check CORS settings in backend
- Ensure both services are deployed

## 🚀 Advantages of Railway

- ✅ **All-in-One**: Database + Backend + Frontend
- ✅ **Easy Setup**: Simple configuration
- ✅ **Auto-Deploy**: Git push triggers deployment
- ✅ **Internal Networking**: Services can communicate securely
- ✅ **Generous Free Tier**: Perfect for development
- ✅ **No CORS Issues**: Same platform deployment

## 🎊 You're Live!

Your complete PulsePixelTech e-commerce platform with SambaNova AI is now running on Railway! 🚂
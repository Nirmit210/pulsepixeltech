# 🚂 Railway + Vercel Deployment Guide

## 🎯 Complete Deployment with Railway Database (5 minutes)

### Step 1: Setup Railway Database (2 minutes)

1. **Go to Railway**
   - Visit: https://railway.app
   - Click "Start a New Project"
   - Sign up/Login with GitHub

2. **Create PostgreSQL Database**
   - Click "Provision PostgreSQL"
   - Wait for deployment (30 seconds)
   - Click on the PostgreSQL service

3. **Get Connection String**
   - Go to "Variables" tab
   - Find `DATABASE_URL`
   - Click "Copy" button
   - Save this for Step 3

### Step 2: Deploy to Vercel (2 minutes)

1. **Go to Vercel**
   - Visit: https://vercel.com
   - Login with GitHub
   - Click "New Project"

2. **Import Repository**
   - Find `Nirmit210/pulsepixeltech`
   - Click "Import"
   - Keep root directory as default
   - Click "Deploy"

### Step 3: Configure Environment Variables (1 minute)

After Vercel deployment completes:

1. **Go to Project Settings**
   - Click on your project in Vercel dashboard
   - Go to "Settings" → "Environment Variables"

2. **Add Variables** (copy/paste this):

```
NODE_ENV=production
DATABASE_URL=paste_your_railway_connection_string_here
JWT_SECRET=your_super_secret_jwt_key_make_it_very_long_and_secure_at_least_32_characters
SAMBANOVA_API_KEY=1c0e0109-1ee0-456a-8470-ae17fa1643e6
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_gmail_app_password
FRONTEND_URL=https://your-vercel-app.vercel.app
NEXT_PUBLIC_API_URL=https://your-vercel-app.vercel.app
NEXT_PUBLIC_APP_NAME=PulsePixelTech
NEXT_PUBLIC_APP_URL=https://your-vercel-app.vercel.app
PAYMENT_SIMULATION_DELAY=1000
PAYMENT_SUCCESS_RATE=98
MAX_FILE_SIZE=5242880
UPLOAD_PATH=./uploads
```

3. **Update URLs**
   - Replace `your-vercel-app` with your actual Vercel app name
   - Replace `paste_your_railway_connection_string_here` with Railway DATABASE_URL

4. **Redeploy**
   - Go to "Deployments" tab
   - Click "Redeploy" on latest deployment

## 🎉 You're Live!

Your app will be available at: `https://your-app-name.vercel.app`

### 🧪 Test Your Deployment

- **Homepage**: Should load with products and categories
- **API Health**: Visit `/api/health` - should return "OK"
- **Categories**: Visit `/categories` - should show product categories  
- **Chatbot**: Click chat button - should respond with AI
- **Login**: Try demo accounts from homepage

### 📊 Railway Database Management

**Access Railway Dashboard:**
1. Go to https://railway.app
2. Click on your project
3. Click PostgreSQL service
4. Use "Data" tab to view tables
5. Use "Metrics" tab to monitor usage

**Free Tier Limits:**
- ✅ 500 hours/month (plenty for development)
- ✅ 1GB storage
- ✅ Shared CPU
- ✅ 8GB RAM

### 🔧 Database Operations

**View Tables** (after first deployment):
1. Go to Railway → Your Project → PostgreSQL
2. Click "Data" tab
3. You should see tables: User, Product, Category, Order, etc.

**Run Migrations** (if needed):
Railway will automatically run Prisma migrations on deployment.

### 💡 Pro Tips

1. **Monitor Usage**: Check Railway metrics regularly
2. **Backup Data**: Railway provides automatic backups
3. **Scale Up**: Upgrade to Railway Pro ($5/month) when needed
4. **Database Logs**: Check Railway logs for database issues

### 🚨 Troubleshooting

**Database Connection Issues:**
- Verify DATABASE_URL is correct in Vercel
- Check Railway service is running
- Ensure no typos in connection string

**Deployment Fails:**
- Check Vercel function logs
- Verify all environment variables are set
- Ensure Railway database is accessible

**App Not Loading:**
- Check browser console for errors
- Verify NEXT_PUBLIC_ variables are set
- Test API endpoints individually

### 🎊 Success Checklist

- [ ] Railway PostgreSQL database created
- [ ] Vercel app deployed successfully
- [ ] All environment variables configured
- [ ] Database tables created (check Railway Data tab)
- [ ] Homepage loads without errors
- [ ] API endpoints respond correctly
- [ ] Chatbot works with SambaNova AI
- [ ] Login/register functionality works
- [ ] Admin dashboard accessible

## 🔄 Future Updates

**To update your app:**
1. Make changes to your code
2. Push to GitHub: `git push`
3. Vercel automatically redeploys
4. Railway database persists all data

**To upgrade database:**
- Railway Pro: $5/month for unlimited usage
- No code changes needed, just upgrade in Railway dashboard

---

**Total Cost**: $0 (using free tiers)
**Total Time**: ~5 minutes
**Result**: Production-ready e-commerce platform! 🚀

**Railway Database**: ✅ Free PostgreSQL with 1GB storage
**Vercel Hosting**: ✅ Free Next.js + Node.js hosting
**SambaNova AI**: ✅ Intelligent chatbot responses
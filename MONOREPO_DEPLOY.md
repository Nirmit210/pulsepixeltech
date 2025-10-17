# 🚀 One-Click Monorepo Deployment

## ✨ Deploy Frontend + Backend Together (3 minutes)

### Step 1: Setup Database (1 minute)
Choose one free option:

**Option A: Supabase (Recommended)**
1. Go to https://supabase.com
2. Sign up with GitHub
3. Create new project
4. Go to Settings → Database → Copy connection string

**Option B: Neon**
1. Go to https://neon.tech  
2. Sign up with GitHub
3. Create database → Copy connection string

### Step 2: Deploy to Vercel (2 minutes)
1. Go to https://vercel.com
2. Login with GitHub
3. Click "New Project"
4. Import `Nirmit210/pulsepixeltech`
5. **Keep root directory as default** (don't change it)
6. Click "Deploy"

### Step 3: Add Environment Variables
After deployment, go to Settings → Environment Variables and add:

```
NODE_ENV=production
DATABASE_URL=your_postgresql_connection_string_from_step1
JWT_SECRET=your_super_secret_jwt_key_here_make_it_very_long_and_secure
SAMBANOVA_API_KEY=1c0e0109-1ee0-456a-8470-ae17fa1643e6
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password
FRONTEND_URL=https://your-vercel-app-url.vercel.app
NEXT_PUBLIC_API_URL=https://your-vercel-app-url.vercel.app
NEXT_PUBLIC_APP_NAME=PulsePixelTech
NEXT_PUBLIC_APP_URL=https://your-vercel-app-url.vercel.app
```

### Step 4: Redeploy
1. Go to Deployments tab
2. Click "Redeploy" on the latest deployment
3. Wait for completion

## 🎉 Done!
Your complete e-commerce platform is live at one URL:
- **Frontend**: `https://your-app.vercel.app`
- **Backend API**: `https://your-app.vercel.app/api`

## 🧪 Quick Test
- [ ] Visit your app URL - homepage should load
- [ ] Try `/categories` - should show product categories
- [ ] Test chatbot - should respond with AI
- [ ] Try login/register - should work
- [ ] Check `/api/health` - should return API status

## ✅ Advantages of Monorepo Deployment
- ✅ **Single URL** - No CORS issues
- ✅ **Easier Management** - One deployment to rule them all
- ✅ **Cost Effective** - Uses one Vercel project
- ✅ **Simpler Setup** - No need to connect frontend/backend
- ✅ **Better Performance** - No cross-domain requests

## 🔧 Environment Variables Template

Copy and paste this into Vercel Environment Variables:

```
NODE_ENV=production
DATABASE_URL=postgresql://user:pass@host:port/database
JWT_SECRET=generate_a_very_long_secure_random_string_at_least_32_characters_long
SAMBANOVA_API_KEY=1c0e0109-1ee0-456a-8470-ae17fa1643e6
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_gmail_app_password
FRONTEND_URL=https://your-app-name.vercel.app
NEXT_PUBLIC_API_URL=https://your-app-name.vercel.app
NEXT_PUBLIC_APP_NAME=PulsePixelTech
NEXT_PUBLIC_APP_URL=https://your-app-name.vercel.app
PAYMENT_SIMULATION_DELAY=1000
PAYMENT_SUCCESS_RATE=98
MAX_FILE_SIZE=5242880
UPLOAD_PATH=./uploads
```

## 🆘 Troubleshooting

**Build Fails?**
- Check Vercel function logs
- Ensure all environment variables are set
- Verify database connection string

**API Not Working?**
- Test `/api/health` endpoint
- Check environment variables
- Verify database is accessible

**Frontend Issues?**
- Clear browser cache
- Check console for errors
- Verify NEXT_PUBLIC_ variables are set

## 🎊 Success!
You now have a complete e-commerce platform with:
- ✅ AI-powered chatbot (SambaNova)
- ✅ Full shopping cart and checkout
- ✅ Admin dashboard
- ✅ Payment simulation
- ✅ Email notifications
- ✅ PWA capabilities
- ✅ Dark mode support

**Total deployment time**: ~3 minutes
**Total cost**: $0 (free tiers)
**Result**: Production-ready e-commerce platform! 🚀
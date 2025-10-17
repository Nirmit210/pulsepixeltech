# 🚀 Vercel Deployment Guide

## Prerequisites
- Vercel account
- GitHub repository
- PostgreSQL database (Supabase/Neon recommended)
- SambaNova API key

## 🔧 Backend Deployment (API)

### 1. Database Setup
Choose one of these PostgreSQL providers:

**Option A: Supabase (Recommended)**
1. Go to [supabase.com](https://supabase.com)
2. Create new project
3. Copy the connection string from Settings > Database

**Option B: Neon**
1. Go to [neon.tech](https://neon.tech)
2. Create new project
3. Copy the connection string

### 2. Deploy Backend to Vercel
1. Push your code to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Import your repository
4. Select the `backend` folder as root directory
5. Add environment variables:

```
NODE_ENV=production
DATABASE_URL=your_postgresql_connection_string
JWT_SECRET=your_very_long_secure_jwt_secret_here
SAMBANOVA_API_KEY=your_sambanova_api_key
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password
PAYMENT_SIMULATION_DELAY=1000
PAYMENT_SUCCESS_RATE=98
MAX_FILE_SIZE=5242880
UPLOAD_PATH=./uploads
FRONTEND_URL=https://your-frontend-domain.vercel.app
```

6. Deploy!

### 3. Database Migration
After backend deployment:
1. Go to your Vercel project dashboard
2. Open the Functions tab
3. Run database migration via Vercel CLI or manually:

```bash
# Install Vercel CLI
npm i -g vercel

# Login to Vercel
vercel login

# Link your project
vercel link

# Run database migration
vercel env pull .env.local
npx prisma migrate deploy
npx prisma db seed
```

## 🎨 Frontend Deployment

### 1. Deploy Frontend to Vercel
1. In Vercel dashboard, create new project
2. Import your repository again
3. Select the `frontend` folder as root directory
4. Add environment variables:

```
NEXT_PUBLIC_API_URL=https://your-backend-domain.vercel.app
NEXT_PUBLIC_APP_NAME=PulsePixelTech
NEXT_PUBLIC_APP_URL=https://your-frontend-domain.vercel.app
```

5. Deploy!

## 🔗 Connect Frontend & Backend

### Update CORS Settings
After both deployments, update your backend CORS configuration:

1. Go to `backend/server.js`
2. Update CORS to allow your frontend domain:

```javascript
app.use(cors({
  origin: [
    'http://localhost:3000',
    'https://your-frontend-domain.vercel.app'
  ],
  credentials: true
}));
```

3. Redeploy backend

## 🧪 Testing Deployment

### 1. Test Backend API
Visit: `https://your-backend-domain.vercel.app/api/health`
Should return: `{"status":"OK","message":"PulsePixelTech API is running"}`

### 2. Test Frontend
Visit: `https://your-frontend-domain.vercel.app`
- All pages should load
- Categories should display
- Chatbot should work
- Login/register should function

### 3. Test Integration
- Try logging in
- Add products to cart
- Test chatbot functionality
- Verify all API calls work

## 🔧 Environment Variables Reference

### Backend (.env)
```
NODE_ENV=production
DATABASE_URL=postgresql://user:pass@host:port/db
JWT_SECRET=your_jwt_secret_min_32_chars
JWT_EXPIRE=7d
SAMBANOVA_API_KEY=your_sambanova_key
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password
PAYMENT_SIMULATION_DELAY=1000
PAYMENT_SUCCESS_RATE=98
MAX_FILE_SIZE=5242880
UPLOAD_PATH=./uploads
FRONTEND_URL=https://your-frontend.vercel.app
```

### Frontend (.env.local)
```
NEXT_PUBLIC_API_URL=https://your-backend.vercel.app
NEXT_PUBLIC_APP_NAME=PulsePixelTech
NEXT_PUBLIC_APP_URL=https://your-frontend.vercel.app
```

## 🚨 Troubleshooting

### Common Issues

**1. Database Connection Error**
- Verify DATABASE_URL is correct
- Check if database allows external connections
- Ensure Prisma schema is deployed

**2. CORS Error**
- Add your frontend domain to CORS whitelist
- Redeploy backend after CORS changes

**3. Environment Variables Not Loading**
- Verify all variables are set in Vercel dashboard
- Check variable names match exactly
- Redeploy after adding variables

**4. Build Failures**
- Check build logs in Vercel dashboard
- Ensure all dependencies are in package.json
- Verify Node.js version compatibility

**5. API Routes Not Working**
- Ensure backend vercel.json is configured correctly
- Check function timeout settings
- Verify route paths match

### Performance Optimization

**1. Database Optimization**
- Add database indexes for frequently queried fields
- Use connection pooling
- Optimize Prisma queries

**2. Frontend Optimization**
- Enable Next.js image optimization
- Use dynamic imports for large components
- Implement proper caching headers

**3. API Optimization**
- Implement response caching
- Use compression middleware
- Optimize database queries

## 📊 Monitoring

### Vercel Analytics
- Enable Vercel Analytics in project settings
- Monitor performance and usage
- Set up alerts for errors

### Database Monitoring
- Monitor database performance
- Set up connection limits
- Track query performance

## 🔄 CI/CD Pipeline

### Automatic Deployments
- Connect GitHub repository
- Enable automatic deployments on push
- Set up preview deployments for PRs

### Environment Branches
- Production: main branch
- Staging: develop branch
- Preview: feature branches

## 🎉 Success Checklist

After successful deployment, verify:

- ✅ Backend API responds at `/api/health`
- ✅ Frontend loads without errors
- ✅ Database connection works
- ✅ User authentication functions
- ✅ Product catalog displays
- ✅ Shopping cart works
- ✅ Chatbot responds (SambaNova AI)
- ✅ Payment simulation works
- ✅ Email notifications send
- ✅ Admin dashboard accessible
- ✅ PWA features work
- ✅ All environment variables set

## 📞 Support

If you encounter issues:
1. Check Vercel function logs
2. Verify environment variables
3. Test API endpoints individually
4. Check database connectivity
5. Review CORS configuration

Your PulsePixelTech e-commerce platform is now live on Vercel! 🎊
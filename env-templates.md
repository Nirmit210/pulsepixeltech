# 📋 Environment Variables Templates

## Backend Environment Variables (Copy & Paste)

```
NODE_ENV=production
DATABASE_URL=paste_your_railway_database_url_here
JWT_SECRET=your_super_secret_jwt_key_here_make_it_very_long_and_secure_for_production_use_at_least_32_characters
SAMBANOVA_API_KEY=1c0e0109-1ee0-456a-8470-ae17fa1643e6
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password
PAYMENT_SIMULATION_DELAY=1000
PAYMENT_SUCCESS_RATE=98
MAX_FILE_SIZE=5242880
UPLOAD_PATH=./uploads
FRONTEND_URL=https://your-vercel-app.vercel.app
```

## Frontend Environment Variables (Copy & Paste)

```
NEXT_PUBLIC_API_URL=https://your-backend-domain.vercel.app
NEXT_PUBLIC_APP_NAME=PulsePixelTech
NEXT_PUBLIC_APP_URL=https://your-frontend-domain.vercel.app
```

## 🗄️ Database Setup

### Railway PostgreSQL (Recommended)
1. Go to https://railway.app
2. Sign up with GitHub
3. "Start a New Project" → "Provision PostgreSQL"
4. Click PostgreSQL service → Variables tab
5. Copy DATABASE_URL value
6. Use in Vercel environment variables

### Alternative Options
See [FREE_DATABASE_OPTIONS.md](./FREE_DATABASE_OPTIONS.md) for other free PostgreSQL providers

## 📧 Email Setup (Optional)
For Gmail SMTP:
1. Enable 2-factor authentication
2. Generate App Password
3. Use App Password as EMAIL_PASS

## 🔐 JWT Secret Generator
Use this command to generate secure JWT secret:
```bash
node -e "console.log(require('crypto').randomBytes(64).toString('hex'))"
```

Or use online generator: https://generate-secret.vercel.app/64
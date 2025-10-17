# 📋 Environment Variables Templates

## Backend Environment Variables (Copy & Paste)

```
NODE_ENV=production
DATABASE_URL=postgresql://postgres:password@localhost:5432/pulsepixeltech
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
FRONTEND_URL=https://your-frontend-domain.vercel.app
```

## Frontend Environment Variables (Copy & Paste)

```
NEXT_PUBLIC_API_URL=https://your-backend-domain.vercel.app
NEXT_PUBLIC_APP_NAME=PulsePixelTech
NEXT_PUBLIC_APP_URL=https://your-frontend-domain.vercel.app
```

## 🗄️ Free Database Options

### Option 1: Supabase (Recommended)
1. Go to https://supabase.com
2. Sign up with GitHub
3. Create new project
4. Go to Settings → Database
5. Copy connection string
6. Use as DATABASE_URL

### Option 2: Neon
1. Go to https://neon.tech
2. Sign up with GitHub  
3. Create database
4. Copy connection string
5. Use as DATABASE_URL

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
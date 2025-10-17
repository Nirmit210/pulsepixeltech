# ⚡ 5-Minute Deployment Checklist

## ✅ Pre-Deployment (2 minutes)

### 1. Create Database (Choose One)
- [ ] **Supabase**: Go to supabase.com → New Project → Copy connection string
- [ ] **Neon**: Go to neon.tech → New Database → Copy connection string

### 2. Prepare Environment Variables
- [ ] Copy backend variables from `env-templates.md`
- [ ] Replace `DATABASE_URL` with your database connection string
- [ ] Generate secure JWT secret (use crypto generator)
- [ ] Keep SambaNova API key as provided

## 🚀 Vercel Deployment (3 minutes)

### Step 1: Deploy Backend
1. [ ] Go to https://vercel.com
2. [ ] Login with GitHub
3. [ ] New Project → Import `Nirmit210/pulsepixeltech`
4. [ ] Root Directory: `backend`
5. [ ] Framework: Other
6. [ ] Deploy
7. [ ] Add environment variables from template
8. [ ] Copy backend URL

### Step 2: Deploy Frontend  
1. [ ] New Project → Import `Nirmit210/pulsepixeltech` (again)
2. [ ] Root Directory: `frontend`
3. [ ] Framework: Next.js
4. [ ] Deploy
5. [ ] Add environment variables (use backend URL from step 1)
6. [ ] Copy frontend URL

### Step 3: Connect Frontend & Backend
1. [ ] Update backend `FRONTEND_URL` with frontend URL
2. [ ] Redeploy backend
3. [ ] Test: Visit your frontend URL

## 🎉 Success!
Your PulsePixelTech e-commerce platform is now live!

## 🧪 Quick Test
- [ ] Homepage loads
- [ ] Categories page works
- [ ] Login/Register functions
- [ ] Chatbot responds
- [ ] Admin dashboard accessible

## 🆘 If Something Goes Wrong
1. Check Vercel function logs
2. Verify environment variables
3. Ensure database is accessible
4. Check CORS settings

## 📞 Need Help?
- Vercel Docs: https://vercel.com/docs
- Supabase Docs: https://supabase.com/docs
- GitHub Issues: Create issue in your repository

---

**Total Time**: ~5 minutes
**Cost**: $0 (using free tiers)
**Result**: Full production e-commerce platform! 🎊
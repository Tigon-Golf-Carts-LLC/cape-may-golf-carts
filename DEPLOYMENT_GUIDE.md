# Cape May Golf Carts - GitHub Deployment Guide

## Step 1: Create GitHub Repository

1. Go to [GitHub.com](https://github.com) and log into your account
2. Click the "+" icon in the top right corner and select "New repository"
3. Repository settings:
   - **Repository name:** `cape-may-golf-carts`
   - **Description:** `Cape May County's premier golf cart dealership website - DENAGO & EVOLUTION electric golf carts`
   - **Visibility:** Public (recommended for business websites)
   - **Initialize:** ✅ Add a README file
   - **Add .gitignore:** Node
   - **Choose a license:** MIT License (optional)

## Step 2: Prepare Local Environment

Open your terminal/command prompt and run:

```bash
# Clone your new repository
git clone https://github.com/YOURUSERNAME/cape-may-golf-carts.git
cd cape-may-golf-carts

# Copy all files from your Replit project to this directory
# (See file list below)
```

## Step 3: Files to Copy from Replit

### Core Configuration Files
```
├── package.json
├── package-lock.json
├── tsconfig.json
├── tailwind.config.ts
├── postcss.config.js
├── components.json
├── drizzle.config.ts
├── vite.config.ts
├── .gitignore
├── README.md
├── replit.md
└── DEPLOYMENT_GUIDE.md
```

### Source Code Directories
```
├── client/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── lib/
│   │   ├── App.tsx
│   │   ├── main.tsx
│   │   └── index.css
├── server/
│   ├── data/
│   ├── index.ts
│   ├── routes.ts
│   ├── storage.ts
│   └── vite.ts
├── shared/
│   └── schema.ts
```

### Static Assets
```
├── public/
│   ├── sitemap.xml
│   ├── robots.txt
│   ├── business-schema.json
│   ├── google-business-verification.html
│   ├── favicon.png
│   └── favicon.jpg
├── attached_assets/
│   └── [All image files - 100+ product images]
```

## Step 4: Environment Setup

Create `.env.example` file:
```
DATABASE_URL=postgresql://username:password@hostname:port/database
NODE_ENV=development
PORT=5000
```

Create `.env` file with your actual values (this will be ignored by Git).

## Step 5: Commit and Push

```bash
# Add all files
git add .

# Commit with descriptive message
git commit -m "Initial commit: Cape May Golf Carts website

- Complete town-specific pages for all 12 Cape May County locations
- Full vehicle inventory: 24+ DENAGO & EVOLUTION models
- SEO optimization: sitemap.xml, business schema, structured data
- Mobile-responsive design with Tailwind CSS
- PostgreSQL database with Drizzle ORM
- Contact forms and service management
- Google My Business integration ready"

# Push to GitHub
git push origin main
```

## Step 6: Deploy to Production

### Option A: Vercel (Recommended)
1. Go to [vercel.com](https://vercel.com) and connect your GitHub
2. Import your `cape-may-golf-carts` repository
3. Configure environment variables:
   - `DATABASE_URL`: Your PostgreSQL connection string
   - `NODE_ENV`: production
4. Deploy automatically

### Option B: Netlify
1. Go to [netlify.com](https://netlify.com) and connect GitHub
2. Choose your repository
3. Build settings:
   - Build command: `npm run build`
   - Publish directory: `dist/public`
4. Add environment variables in site settings

### Option C: Railway
1. Go to [railway.app](https://railway.app)
2. Connect GitHub repository
3. Add PostgreSQL database
4. Set environment variables
5. Deploy automatically

## Step 7: Database Setup

After deployment, run database migrations:
```bash
npm run db:push
```

## Step 8: Domain Configuration

1. Purchase domain: `capemaygolfcarts.com`
2. Configure DNS in your hosting platform
3. Enable SSL/TLS certificates
4. Update sitemap URLs in `sitemap.xml`

## Step 9: SEO Setup

1. **Google Search Console:**
   - Add property for your domain
   - Submit `sitemap.xml`
   - Verify ownership

2. **Google My Business:**
   - Create/claim business listing
   - Use `/google-business-verification.html`
   - Add photos and business hours

3. **Analytics:**
   - Set up Google Analytics
   - Add tracking code to all pages

## Files Summary

**Total Files:** 150+
- React components: 25+
- Vehicle images: 100+
- Town pages: 12
- Vehicle detail pages: 24
- SEO files: 4
- Configuration files: 10+

## Repository Features

✅ Complete town-specific landing pages
✅ Full vehicle inventory with specifications
✅ Mobile-responsive design
✅ SEO-optimized with structured data
✅ Contact form integration
✅ Database schema and migrations
✅ Production-ready configuration

## Support

After deployment:
- Test all 12 town pages
- Verify vehicle detail pages
- Test contact forms
- Check sitemap accessibility
- Confirm mobile responsiveness

Your Cape May Golf Carts website will be live and ready to serve customers across Cape May County!
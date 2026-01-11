# GitHub Pages Deployment Guide

## Quick Setup (5 minutes)

### Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the **"+"** icon → **"New repository"**
3. Repository name: `moneybook-legal` (or any name you prefer)
4. Set to **Public** (required for free GitHub Pages)
5. Click **"Create repository"**

### Step 2: Upload Files

You have two options:

#### Option A: Using GitHub Web Interface (Easiest)

1. In your new repository, click **"uploading an existing file"**
2. Drag and drop all files from the `docs` folder:
   - `index.html`
   - `privacy-policy.html`
   - `terms-of-service.html`
   - `styles.css`
3. Scroll down and click **"Commit changes"**

#### Option B: Using Git Command Line

```bash
# Navigate to your project
cd C:\Users\1muha\Music\money_book

# Initialize git if not already done
git init

# Add the remote repository (replace YOUR_USERNAME with your GitHub username)
git remote add legal-origin https://github.com/YOUR_USERNAME/moneybook-legal.git

# Add only the docs folder
git add docs/

# Commit
git commit -m "Add legal documentation"

# Push to GitHub
git push -u legal-origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **"Settings"** tab
3. Scroll down to **"Pages"** in the left sidebar
4. Under **"Source"**, select:
   - Branch: `main`
   - Folder: `/ (root)` or `/docs` (depending on where you uploaded)
5. Click **"Save"**

### Step 4: Wait for Deployment

- GitHub will build your site (takes 1-2 minutes)
- You'll see a message: **"Your site is live at https://YOUR_USERNAME.github.io/moneybook-legal/"**
- Visit the URL to verify

---

## Your URLs After Deployment

Once deployed, your legal documents will be accessible at:

- **Landing Page:** `https://YOUR_USERNAME.github.io/moneybook-legal/`
- **Privacy Policy:** `https://YOUR_USERNAME.github.io/moneybook-legal/privacy-policy.html`
- **Terms of Service:** `https://YOUR_USERNAME.github.io/moneybook-legal/terms-of-service.html`

---

## What to Do Next

### 1. Update Google Play Console

When you submit your app to Google Play:

1. Go to **Store listing** → **Privacy policy**
2. Enter your Privacy Policy URL:
   ```
   https://YOUR_USERNAME.github.io/moneybook-legal/privacy-policy.html
   ```

### 2. Add Links in Your App (Optional but Recommended)

You can link to these pages from your app's:
- Login screen (already has a `LegalScreen` - we'll update it)
- Settings screen
- About section

### 3. Update the Contact Email

**IMPORTANT:** The legal documents currently use `support@moneybook.app` as the contact email.

You need to either:
- **Create this email address**, OR
- **Replace it** with your actual support email in all three HTML files

To replace:
1. Open each HTML file (`privacy-policy.html`, `terms-of-service.html`, `index.html`)
2. Find: `support@moneybook.app`
3. Replace with your real email (e.g., `your.email@gmail.com`)

### 4. Update Governing Law (Terms of Service)

In `terms-of-service.html`, find section **12.1 Governing Law**:
```html
<p>These Terms shall be governed by and construed in accordance with the laws of [Your Jurisdiction]...</p>
```

Replace `[Your Jurisdiction]` with your actual jurisdiction, for example:
- `the State of California, United States`
- `India`
- `the United Kingdom`

---

## Custom Domain (Optional)

If you own a domain (e.g., `moneybook.app`), you can use it instead:

1. In your repository settings → Pages
2. Enter your custom domain
3. Add DNS records as instructed by GitHub
4. Your URLs will be: `https://moneybook.app/privacy-policy.html`

---

## Updating the Legal Documents

Whenever you need to make changes:

1. Edit the HTML files locally
2. Update the "Last Updated" date
3. Upload/push to GitHub
4. Changes will be live in 1-2 minutes
5. **Important:** Notify users of significant changes (via app notification or email)

---

## Alternative: Use Your Main Repository

If you prefer to host the legal pages in your main MoneyBook repository:

1. Keep the `docs` folder in your existing repository
2. Push to your main GitHub repo
3. In Settings → Pages, select:
   - Branch: `main`
   - Folder: `/docs`
4. URL will be: `https://YOUR_USERNAME.github.io/money_book/`

---

## Verification Checklist

Before submitting to Google Play, verify:

- [ ] Privacy Policy loads correctly
- [ ] Terms of Service loads correctly
- [ ] All links work (navigation between pages)
- [ ] Contact email is correct and active
- [ ] Governing law jurisdiction is specified
- [ ] "Last Updated" date is current
- [ ] Pages are mobile-friendly (test on phone)
- [ ] HTTPS is enabled (GitHub Pages uses HTTPS by default)

---

## Troubleshooting

### "404 - Page Not Found"
- Wait 2-3 minutes after enabling Pages
- Check that files are in the root or `/docs` folder as configured
- Verify branch name is correct (main vs master)

### "Privacy Policy URL is invalid" (Google Play Console)
- Ensure URL starts with `https://`
- URL must be publicly accessible (not behind login)
- Test URL in incognito/private browser window

### Want to Use a Subdomain?
- If you own `moneybook.com`, you can set up `legal.moneybook.com`
- Requires DNS configuration and custom domain setup in GitHub Pages

---

## Need Help?

- **GitHub Pages Documentation:** https://docs.github.com/en/pages
- **Support:** If you encounter issues, let me know!

---

## What's Included in These Legal Documents

### Privacy Policy ✅
- ✅ Firebase services disclosure
- ✅ Google Sign-In data collection
- ✅ GDPR compliance (EU users)
- ✅ CCPA compliance (California users)
- ✅ Data retention and deletion policy
- ✅ International data transfers
- ✅ Children's privacy (age 13+)
- ✅ Security measures
- ✅ Contact information
- ✅ Account deletion process

### Terms of Service ✅
- ✅ Service description
- ✅ Account management
- ✅ Subscription terms (for future use)
- ✅ Account deletion process
- ✅ Financial disclaimer
- ✅ Liability limitations
- ✅ Intellectual property
- ✅ Dispute resolution

**Both documents are fully compliant with Google Play requirements!**

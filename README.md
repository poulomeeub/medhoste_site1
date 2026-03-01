# MedHoste — Healthcare Logistics Website
> Deploy guide for GitHub Pages · No coding experience required

---

## 📁 What's In This Folder

```
medhoste-site/
├── index.html      ← Your full website (all pages in one file)
├── 404.html        ← Custom "page not found" screen
├── robots.txt      ← Tells Google how to index your site
├── sitemap.xml     ← Helps Google find your pages
└── README.md       ← This guide
```

---

## 🚀 STEP-BY-STEP: Go Live on GitHub Pages

### STEP 1 — Create a GitHub account
1. Go to **https://github.com**
2. Click **Sign up** (top right)
3. Enter your email, create a password, choose a username
   - Pick something professional, e.g. `medhoste` or `clement-omoh`
   - Your site URL will be: `https://YOUR-USERNAME.github.io/medhoste-site`
4. Verify your email address

---

### STEP 2 — Create a new repository
1. Once logged in, click the **green "New"** button (or go to https://github.com/new)
2. Fill in:
   - **Repository name:** `medhoste-site`
   - **Description:** `MedHoste Healthcare Logistics Website`
   - Set to **Public** ← (required for free GitHub Pages)
   - ✅ Check **"Add a README file"**
3. Click **"Create repository"**

---

### STEP 3 — Upload your files
1. Inside your new repository, click **"Add file"** → **"Upload files"**
2. Drag and drop ALL files from this folder:
   - `index.html`
   - `404.html`
   - `robots.txt`
   - `sitemap.xml`
3. At the bottom, in the **"Commit changes"** box, type:
   `Initial website upload`
4. Click **"Commit changes"** (green button)

---

### STEP 4 — Enable GitHub Pages
1. In your repository, click **"Settings"** (top menu bar)
2. In the left sidebar, scroll down and click **"Pages"**
3. Under **"Source"**, click the dropdown and select **"Deploy from a branch"**
4. Under **"Branch"**, select **"main"** and folder **"/ (root)"**
5. Click **"Save"**
6. Wait 1–2 minutes, then refresh the page
7. You will see a green box with your live URL:
   **`https://YOUR-USERNAME.github.io/medhoste-site`** 🎉

---

## ✏️ UPDATING YOUR WEBSITE LATER

When you want to make changes:
1. Edit `index.html` on your computer
2. Go to your GitHub repository
3. Click on `index.html` in the file list
4. Click the **pencil icon** (Edit) top right
5. Paste your updated code
6. Click **"Commit changes"**
7. Your live site updates automatically in ~1 minute

---

## 📬 ADDING THE CONTACT FORM (Formspree) — When You're Ready

When you want the contact form to actually send you emails, follow these steps:

### Step 1 — Create a Formspree account
1. Go to **https://formspree.io**
2. Click **"Get Started Free"**
3. Sign up with your email (the one you want form submissions sent to)

### Step 2 — Create a new form
1. In your Formspree dashboard, click **"+ New Form"**
2. Name it: `MedHoste Pickup Request`
3. Formspree will give you a **Form ID** that looks like: `xpwzabcd`
4. Copy that ID

### Step 3 — Update your website code
In your `index.html`, find this line (around line 430):
```html
<button type="submit" class="btn-primary" style="width:100%; text-align:center; cursor:pointer; border:none; font-size:0.95rem;">Submit Pickup Request</button>
```

**Above** that button, add this hidden input:
```html
<input type="hidden" name="_subject" value="New MedHoste Pickup Request">
<input type="hidden" name="_next" value="https://YOUR-USERNAME.github.io/medhoste-site/?submitted=true">
```

Then find the line:
```html
<button type="submit" ...
```

And wrap the entire form in:
```html
<form action="https://formspree.io/f/YOUR-FORM-ID" method="POST">
  ... all your form fields ...
</form>
```

Replace `YOUR-FORM-ID` with the ID from Formspree (e.g. `xpwzabcd`).

### Step 4 — Done!
Every time someone submits the form, Formspree will:
- ✅ Email you the submission instantly
- ✅ Store it in your Formspree dashboard
- ✅ Redirect the user to a thank-you page

**Free Formspree plan:** 50 submissions/month — plenty to start.

---

## 🌐 ADDING A CUSTOM DOMAIN LATER (e.g. medhoste.com)

When you're ready to use a real domain:

1. Buy your domain at **Namecheap.com** or **GoDaddy.com**
2. In your GitHub repository → **Settings → Pages → Custom domain**
3. Type in your domain (e.g. `medhoste.com`) and click Save
4. In your domain registrar's DNS settings, add these records:

| Type  | Host | Value                  |
|-------|------|------------------------|
| A     | @    | 185.199.108.153        |
| A     | @    | 185.199.109.153        |
| A     | @    | 185.199.110.153        |
| A     | @    | 185.199.111.153        |
| CNAME | www  | YOUR-USERNAME.github.io |

5. Wait up to 24 hours for DNS to propagate
6. ✅ Check **"Enforce HTTPS"** in GitHub Pages settings for the padlock 🔒

---

## 📞 Your Contact Details To Update in index.html

Search for these placeholders and replace with your real info:

| Placeholder | Replace With |
|------------|--------------|
| `1-800-MED-HOST` | Your real phone number |
| `info@medhoste.com` | Your real email |
| `partnerships@medhoste.com` | Your real email |
| `compliance@medhoste.com` | Your real email |
| `support@medhoste.com` | Your real email |
| `YOUR-USERNAME` | Your GitHub username |

---

## ✅ PRE-LAUNCH CHECKLIST

Before sharing your URL publicly:

- [ ] Replace all phone numbers with real numbers
- [ ] Replace all email addresses with real emails
- [ ] Update the founder name/bio if needed
- [ ] Test the site on your phone (mobile view)
- [ ] Test all nav links scroll to correct sections
- [ ] Replace testimonials with real client quotes when available
- [ ] Update `robots.txt` and `sitemap.xml` with your real GitHub username

---

## 🆘 Need Help?

If you get stuck at any step, Google: **"GitHub Pages not working [your issue]"** — the GitHub community is very active and beginner-friendly.

Official GitHub Pages docs: https://docs.github.com/en/pages

---

*MedHoste Healthcare Logistics — Secure. Timely. Compliant.*

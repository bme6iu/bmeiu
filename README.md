# 🏥 IU Department of Biomedical Engineering — Website

> Premium department website for Islamic University Bangladesh, hosted on GitHub Pages with Decap CMS for easy content management.

---

## 🚀 Live Setup Guide

### Step 1: GitHub Repository তৈরি করুন

```bash
# GitHub-এ একটি নতুন repository তৈরি করুন, নাম দিন:
# bme.iu.ac.bd   অথবা   iu-bme-website

# তারপর ফাইলগুলো push করুন:
git init
git add .
git commit -m "Initial BME website"
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

### Step 2: GitHub Pages চালু করুন

1. Repository → **Settings** → **Pages**
2. Source: **Deploy from branch** → `main` → `/ (root)`
3. Save করুন
4. কিছুক্ষণ পরে আপনার সাইট `https://YOUR_USERNAME.github.io/YOUR_REPO/` এ লাইভ হবে

### Step 3: `admin/config.yml` আপডেট করুন

```yaml
backend:
  name: github
  repo: YOUR_USERNAME/YOUR_REPO  # ← এটা বদলান
  branch: main
```

### Step 4: CMS Login সেটআপ (Decap CMS + Netlify OAuth)

**Option A — Netlify OAuth (সবচেয়ে সহজ, বিনামূল্যে):**

1. [netlify.com](https://netlify.com) এ একটি বিনামূল্যে অ্যাকাউন্ট তৈরি করুন
2. **Sites** → **Add new site** → **Import an existing project** → GitHub repo সিলেক্ট করুন
3. Netlify site deploy হলে: **Site settings** → **Identity** → **Enable Identity**
4. **Identity** → **Registration** → **Invite only** (শুধু অনুমোদিত ইমেইল)
5. **Identity** → **Services** → **Git Gateway** → **Enable**
6. এখন `/admin/` URL-এ গেলে GitHub দিয়ে login করতে পারবেন

**Option B — GitHub OAuth App (advanced):**
- GitHub → Settings → Developer Settings → OAuth Apps → New OAuth App
- Homepage URL: আপনার সাইটের URL
- Authorization callback URL: `https://api.netlify.com/auth/done`

---

## 📁 ফাইল স্ট্রাকচার

```
/
├── index.html              ← মূল ওয়েবসাইট (সম্পূর্ণ single-page)
├── admin/
│   ├── index.html          ← CMS Admin Panel
│   └── config.yml          ← CMS Configuration
├── _data/                  ← CMS এর ডেটা এখানে সেভ হবে
│   ├── notices/            ← নোটিশ ফাইল (.yml)
│   ├── news/               ← খবর ফাইল (.yml)
│   ├── faculty/            ← শিক্ষকদের প্রোফাইল (.yml)
│   ├── courses/            ← কোর্স তথ্য (.yml)
│   ├── collaborations/     ← আন্তর্জাতিক সহযোগিতা
│   ├── batches/            ← ব্যাচ তথ্য
│   ├── alumni/             ← অ্যালামনাই
│   └── settings/
│       └── general.yml     ← সাইটের সাধারণ তথ্য
└── assets/
    └── uploads/            ← ছবি ও ডকুমেন্ট আপলোড
```

---

## ✏️ কন্টেন্ট এডিট করবেন কীভাবে?

### CMS দিয়ে (সহজ):
1. `https://yoursite.com/admin/` → Login করুন
2. বাম পাশে মেনু থেকে যা edit করতে চান সিলেক্ট করুন
3. Edit → Save → Publish
4. GitHub এ automatically commit হবে এবং সাইট আপডেট হবে

### সরাসরি GitHub থেকে:
- `_data/notices/` ফোল্ডারে নতুন `.yml` ফাইল তৈরি করুন
- Format অনুসরণ করুন, push করুন — সাইট আপডেট হবে

---

## 🔧 Customization

### রং পরিবর্তন:
`index.html` এর `:root` সেকশনে CSS variables বদলান:
```css
--teal: #0EA5E9;    /* প্রধান accent রং */
--navy: #0A1628;    /* dark রং */
--gold: #F59E0B;    /* secondary accent */
```

### লোগো:
`index.html` এ `nav-logo` SVG অংশটি বিশ্ববিদ্যালয়ের আসল লোগো দিয়ে বদলান।

---

## 📊 Features Summary

| Feature | Status |
|---------|--------|
| Responsive (Mobile + Desktop) | ✅ |
| Light Premium Theme | ✅ |
| Decap CMS Integration | ✅ |
| GitHub Pages Compatible | ✅ |
| ECG Hero Animation | ✅ |
| Faculty Profiles | ✅ |
| Course Curriculum | ✅ |
| Lab Facilities | ✅ |
| International Collaborations | ✅ |
| Student Batches & Alumni | ✅ |
| News & Notice Board | ✅ |
| Scroll Animations | ✅ |
| Dark Nav + Hero | ✅ |
| Active Nav Links | ✅ |
| Scroll-to-Top Button | ✅ |

---

## 📞 Support

Department of Biomedical Engineering  
Islamic University, Kushtia-Jhenaidah 7003  
Email: bme@iu.ac.bd

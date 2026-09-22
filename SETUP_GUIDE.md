# 🚀 Setup Guide: itzlucifa GitHub Profile

## Overview
This creates a **professional, animated GitHub profile** at `github.com/itzlucifa` with:
- 🎨 Animated gradient header + typing animation
- 📊 Live GitHub stats (auto-updated daily)
- 🐍 Snake eating your contribution graph
- 🌈 3D rainbow contribution graph
- 📈 Detailed metrics (lowlighter/metrics)
- 🏆 GitHub trophies
- 🛠️ Tech stack with skill icons

---

## 📋 Prerequisites

1. **GitHub Account**: `itzlucifa` (already have)
2. **Git installed** locally
3. **Node.js 18+** (for local testing if needed)

---

## 🛠️ Step-by-Step Setup

### 1. Create the Profile Repository

```bash
# Go to GitHub and create a NEW repository:
# Repository name: itzlucifa (MUST match your username exactly!)
# Description: My GitHub Profile ✨
# Public: ✅
# Initialize with README: ❌ (we have our own)
```

### 2. Push the Profile Files

```bash
# Navigate to the created profile folder
cd C:\Users\asus\OneDrive\Desktop\itzlucifa-profile

# Initialize git and push
git init
git add .
git commit -m "🎉 Initial profile setup with animations, snake, 3D graph, metrics"
git branch -M main
git remote add origin https://github.com/itzlucifa/itzlucifa.git
git push -u origin main
```

### 3. Enable GitHub Actions

After pushing, go to your repo:
1. Click **Actions** tab
2. Click **"I understand my workflows, go ahead and enable them"**
3. You'll see 3 workflows:
   - 🐍 **Generate Snake Animation** (runs daily at midnight UTC)
   - 🌈 **Generate 3D Contribution Graph** (runs daily at 18:00 UTC)
   - 📊 **Generate Metrics** (runs daily at 06:00 UTC)

### 4. Run Workflows Manually (First Time)

Go to **Actions** → Click each workflow → **Run workflow** → **Run workflow**

This generates the initial SVG files in the `dist/` folder.

### 5. Verify It Works

Visit: **https://github.com/itzlucifa**

Your profile should now show:
- ✅ Animated header with your name
- ✅ Typing animation
- ✅ GitHub stats cards
- ✅ Snake animation (after workflow runs)
- ✅ 3D contribution graph (after workflow runs)
- ✅ Detailed metrics (after workflow runs)
- ✅ Tech stack icons
- ✅ Trophies

---

## ⚙️ Customization

### Update Personal Info
Edit `README.md` and change:
- **Name**: `Sumit Nawale` → Your name
- **Bio**: `ENTC Student | Cybersecurity Enthusiast` → Your bio
- **Links**: LinkedIn, Email, Twitter URLs
- **Projects**: Update featured repos in the "Featured Project" section

### Change Color Theme
In `README.md`, replace color values:
```markdown
# Current (Violet → Cyan)
Primary: #7C3AED (violet)
Secondary: #06B6D4 (cyan)

# Alternative themes:
# Dark Red → Orange: #DC2626, #F97316
# Emerald → Teal: #10B981, #14B8A6
# Rose → Pink: #F43F5E, #EC4899
```

### Add/Remove Skills
In the **Tech Stack** section, modify:
```markdown
# Add more icons (see https://skillicons.dev for all options)
<img src="https://skillicons.dev/icons?i=python,typescript,react,rust,go,aws,docker,kubernetes" />
```

### Custom Skills (Non-skillicons)
Add custom badges:
```markdown
<img src="https://img.shields.io/badge/Custom_Tool-FF6B6B?style=for-the-badge&logo=custom&logoColor=white" />
```

---

## 🔧 Troubleshooting

### Snake/3D Graph Not Showing?
1. Check **Actions** tab → ensure workflows ran successfully (green checkmark)
2. Wait 1-2 minutes after workflow completes
3. Hard refresh browser (Ctrl+Shift+R)
4. Check `dist/` folder in repo has `.svg` files

### Metrics Not Loading?
- Metrics uses `lowlighter/metrics` GitHub Action
- First run may take 2-3 minutes
- Check Actions logs for errors

### Stats Cards Showing "Unable to fetch"?
- GitHub API rate limits (wait a bit)
- Ensure repo is **Public**
- Try: `https://github-readme-stats.vercel.app/api?username=itzlucifa` directly

### Want Different Schedule?
Edit `.github/workflows/*.yml`:
```yaml
on:
  schedule:
    - cron: '0 2 * * *'  # Change time (UTC)
```
Use [crontab.guru](https://crontab.guru) to convert.

---

## 📁 File Structure

```
itzlucifa-profile/
├── README.md                    # Main profile (displayed on GitHub)
├── assets/
│   └── wave.svg                 # Footer wave animation
├── .github/
│   └── workflows/
│       ├── snake.yml            # 🐍 Snake animation (daily)
│       ├── profile-3d.yml       # 🌈 3D contribution graph (daily)
│       └── metrics.yml          # 📊 Detailed metrics (daily)
└── dist/                        # Auto-generated (gitignored usually)
    ├── github-contribution-grid-snake.svg
    ├── github-contribution-grid-snake-dark.svg
    ├── 3d-contrib.svg
    └── metrics.svg
```

---

## 🎯 Next Level Enhancements

### Add WakaTime Coding Stats
1. Create account at [wakatime.com](https://wakatime.com)
2. Add `WAKATIME_API_KEY` as **Repository Secret** (Settings → Secrets → Actions)
3. Uncomment wakatime line in README

### Add Blog Posts
Create `.github/workflows/blog.yml`:
```yaml
- name: Latest Blog Posts
  uses: gautamkrishnar/blog-post-workflow@master
  with:
    feed_list: "https://yourblog.com/rss.xml"
```

### Add Spotify Now Playing
Use [spotify-github-profile](https://github.com/kittinan/spotify-github-profile)

### Custom Domain for Profile
Point `itzlucifa.github.io` to your portfolio site

---

## 📞 Need Help?

- **GitHub Actions Docs**: https://docs.github.com/en/actions
- **lowlighter/metrics**: https://github.com/lowlighter/metrics
- **Platane/snk**: https://github.com/Platane/snk
- **Skill Icons**: https://skillicons.dev
- **Readme Typing SVG**: https://github.com/DenverCoder1/readme-typing-svg

---

## ✅ Quick Checklist

- [ ] Repository `itzlucifa/itzlucifa` created (Public)
- [ ] All files pushed to `main` branch
- [ ] GitHub Actions enabled
- [ ] All 3 workflows run manually once
- [ ] Profile visible at `github.com/itzlucifa`
- [ ] Snake animation appears
- [ ] 3D graph appears
- [ ] Metrics appear
- [ ] Personal info customized

---

**🎉 Done!** Your profile is now one of the most creative on GitHub. Star ⭐ the tools that power it: `lowlighter/metrics`, `Platane/snk`, `rahuldkjain/github-profile-readme-generator`
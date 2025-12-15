# 🚀 GitHub Profile README Setup Guide

## Step 1: Create Your Profile Repository

1. Go to [GitHub](https://github.com) and create a **new repository**
2. Name it **exactly** the same as your username: `Abhay-Maheshwari`
3. Make it **Public**
4. Check **"Add a README file"**
5. Click **Create repository**

---

## Step 2: Set Up Personal Access Token (for Metrics)

The metrics workflow requires a Personal Access Token:

1. Go to [GitHub Settings → Developer settings → Personal access tokens → Tokens (classic)](https://github.com/settings/tokens)
2. Click **"Generate new token (classic)"**
3. Name it: `METRICS_TOKEN`
4. Set expiration as needed (or "No expiration")
5. Select these scopes:
   - ✅ `repo` (Full control of private repositories)
   - ✅ `read:user` (Read user profile data)
   - ✅ `read:org` (Read org membership)
6. Click **Generate token**
7. **Copy the token immediately** (you won't see it again!)

---

## Step 3: Add the Token as a Repository Secret

1. Go to your `Abhay-Maheshwari` repository
2. Navigate to **Settings → Secrets and variables → Actions**
3. Click **"New repository secret"**
4. Name: `METRICS_TOKEN`
5. Value: *Paste your token*
6. Click **Add secret**

---

## Step 4: Upload the Files

### Option A: Using Git

```bash
# Clone your profile repo
git clone https://github.com/Abhay-Maheshwari/Abhay-Maheshwari.git
cd Abhay-Maheshwari

# Copy the files from github-profile folder
# Replace the README.md with the one provided
# Copy the .github/workflows/metrics.yml

# Create the metrics folder
mkdir -p metrics

# Commit and push
git add .
git commit -m "✨ Add profile README with metrics"
git push
```

### Option B: Using GitHub Web UI

1. Go to your profile repository
2. Upload `README.md` (replace existing)
3. Create folder `.github/workflows/`
4. Upload `metrics.yml` inside it
5. Create an empty `metrics/` folder (add a `.gitkeep` file)

---

## Step 5: Run the Workflow

1. Go to **Actions** tab in your repository
2. Click on **"GitHub Metrics"** workflow
3. Click **"Run workflow"** → **"Run workflow"**
4. Wait for all jobs to complete (takes 2-5 minutes)

---

## Step 6: Customize!

### Update Social Links
In `README.md`, replace:
- `YOUR_LINKEDIN` → Your LinkedIn username
- `YOUR_TWITTER` → Your Twitter handle
- `your.email@example.com` → Your email
- `YOUR_PORTFOLIO_URL` → Your portfolio website

### Customize Metrics
In `.github/workflows/metrics.yml`, you can:
- Change `config_timezone` to your timezone
- Adjust `plugin_isocalendar_duration` (full-year, half-year, quarter)
- Modify `plugin_activity_limit` for more/fewer activities
- Add more plugins from [metrics documentation](https://github.com/lowlighter/metrics)

---

## 📚 Additional Metrics Plugins You Can Add

Add these to your workflow for more visualizations:

```yaml
# Languages
plugin_languages: yes
plugin_languages_colors: github
plugin_languages_limit: 8

# Achievements
plugin_achievements: yes
plugin_achievements_display: detailed

# Coding Habits
plugin_habits: yes
plugin_habits_charts: yes

# Notable Contributions
plugin_notable: yes
plugin_notable_repositories: yes

# WakaTime Integration
plugin_wakatime: yes
plugin_wakatime_token: ${{ secrets.WAKATIME_TOKEN }}
```

---

## 🎨 Theme Customization

The README uses a purple/indigo theme (`#6366F1`). To change it:

1. Search and replace `6366F1` with your preferred hex color
2. Change `tokyonight` theme to others like:
   - `radical`, `merko`, `gruvbox`, `dracula`, `nord`

---

## 🔗 Useful Resources

- [Metrics Documentation](https://github.com/lowlighter/metrics)
- [Metrics Plugins List](https://metrics.lecoq.io/)
- [GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats)
- [Skill Icons](https://skillicons.dev/)
- [Typing SVG](https://readme-typing-svg.demolab.com/)

---

**Happy Coding! 🎉**

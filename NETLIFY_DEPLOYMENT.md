# Netlify Deployment — Reconnect Repo

**Current Issue:** Netlify is still pointing to the old `firmedge-site` repo. The new website isn't showing.

**Fix:** Reconnect Netlify to the new `matteriq-website` GitHub repo.

---

## Steps (5 minutes)

### 1. Open Netlify Dashboard
Go to: https://app.netlify.com/

### 2. Select Your Site
Find and click on `matteriq-site`

### 3. Go to Build & Deploy Settings
Click **"Site settings"** (top menu) → **"Build & deploy"** → **"Repository"**

### 4. Disconnect Old Repo
Click **"Disconnect repository"** (under the current firmedge-site link)

Confirm the disconnect.

### 5. Connect New Repo
Click **"Connect to Git"**

1. Select **GitHub** as provider
2. Authorize if prompted (use your GitHub account)
3. Search for `matteriq-website`
4. Click `CassMorgan/matteriq-website`
5. Select **main** branch
6. Click **"Deploy site"**

### 6. Verify Deploy Settings
Netlify should auto-detect:
- **Build command:** (leave empty — no build step needed)
- **Publish directory:** `.` (root directory)

If not, manually set these.

### 7. Wait for Rebuild
Netlify will build and deploy. Check the **"Deploys"** tab.

Status should show **green checkmark** in ~30 seconds.

### 8. Verify Live
Visit: https://matteriq-site.netlify.app/

You should see:
- Hero: "Your Law Firm's Smartest Employee"
- Problem section with 6 cards
- ROI calculator link in nav
- `/roi-calculator` page works

---

## Troubleshooting

### "Page not found" on ROI calculator?
→ Netlify hasn't fully deployed yet. Wait 1 minute and refresh.

### Old site still showing?
→ Hard refresh your browser: `Ctrl + Shift + R` (or `Cmd + Shift + R` on Mac)

### Deploy failed?
→ Check the Netlify deploy logs for errors. Usually means a bad file path.

### nav links broken?
→ Make sure you're testing from the root: https://matteriq-site.netlify.app/

---

## Verification Checklist

After Netlify rebuilds:

- [ ] Homepage loads (hero visible)
- [ ] "See Your ROI" button works
- [ ] ROI Calculator link in nav works
- [ ] Calculator loads at `/roi-calculator.html`
- [ ] Calculator inputs update real-time
- [ ] Mobile view looks good
- [ ] All section links in nav work (#problem, #solution, etc.)
- [ ] Contact email in footer is correct

---

## Deploy Status

**Last Commit:** `f9b674e` (Complete website rewrite)  
**Repository:** https://github.com/CassMorgan/matteriq-website  
**Main Branch:** Up to date with latest code  

Once Netlify reconnects, it will automatically pull the latest code from GitHub.

---

## Questions?

If deploy fails:
1. Check Netlify logs for errors
2. Verify repo is public: https://github.com/CassMorgan/matteriq-website
3. Try triggering manual deploy: Site → Deploys → Trigger Deploy

The code is correct. This is just about pointing Netlify to the right GitHub repo.

---

**Once deployed, your website will:**
✅ Show real MatterIQ features  
✅ Calculate personalized ROI for prospects  
✅ Support three pricing tiers  
✅ Drive demos with warm leads  

Go live when ready!

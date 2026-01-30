# 🚀 QUICK DEPLOYMENT GUIDE

## Deploy to Vercel in 3 Steps:

### Option A: Vercel CLI (Fastest)

1. Install Vercel CLI:
   ```bash
   npm install -g vercel
   ```

2. Navigate to this folder in terminal and run:
   ```bash
   vercel
   ```

3. Follow prompts and you're live! 🎉

### Option B: Vercel Website (No Code)

1. Go to https://vercel.com and sign up/login
2. Click "Add New" → "Project"
3. Drag and drop this entire folder
4. Click "Deploy"
5. Done! Your site will be live in seconds! 🎉

### Option C: GitHub Integration

1. Create a new GitHub repository
2. Upload these files to the repository
3. Go to https://vercel.com
4. Click "Import Project" and select your repo
5. Vercel auto-deploys! 🎉

## ✏️ CUSTOMIZE YOUR RESUME

Open `index.html` in any text editor and find the `resumeData` object (around line 280).

Replace the example data with your own:
- Name, title, contact info
- Education
- Skills
- Work experience
- Projects
- Achievements

Save and redeploy!

## 🎨 CUSTOMIZE COLORS

Find the `:root` section in `index.html` (around line 20) and change:
- `--primary`: Main accent color
- `--secondary`: Secondary accent
- `--accent`: Highlight color
- `--dark`: Background color
- `--light`: Text color

## 💡 TIPS

- The site works immediately - just open index.html in a browser to test
- Mobile-friendly automatically
- No build process needed
- All code is in one file for easy editing
- Add more zones by adding objects to the `zones` array

---

**Your VR Resume will be live at: `https://your-project-name.vercel.app`**

Good luck! 🌟

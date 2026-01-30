# 🌌 VR Documentary Resume - Immersive 3D Portfolio

An immersive, documentary-style 3D resume experience built with Three.js. Navigate through a cosmic world where your professional journey comes alive as interactive, glowing orbs representing different aspects of your career.

## ✨ Features

- **Immersive 3D Environment**: Navigate through a beautiful starfield with floating platforms
- **Interactive Zones**: Click on glowing orbs to explore different resume sections:
  - 🎓 Education Hub
  - ⚡ Skills Galaxy
  - 💼 Experience Realm
  - 🚀 Projects Universe
  - 🏆 Achievements Peak
- **Smooth Interactions**: Drag to rotate the camera, hover effects, and smooth animations
- **Responsive Design**: Works on desktop and mobile devices
- **Zero Dependencies**: Pure Three.js with no build step required

## 🎨 Customization

Edit the `resumeData` object in `index.html` (around line 280) to add your own information:

```javascript
const resumeData = {
    name: "Your Name",
    title: "Your Title",
    contact: {
        email: "your.email@example.com",
        linkedin: "linkedin.com/in/yourprofile",
        // ... more contact info
    },
    zones: [
        {
            name: "Education Hub",
            icon: "🎓",
            color: 0x00f3ff,
            position: [-8, 2, 0],
            content: {
                // ... your content
            }
        },
        // ... more zones
    ]
};
```

### Color Customization

You can change the color scheme by modifying the CSS variables at the top of the file:

```css
:root {
    --primary: #00f3ff;    /* Cyan */
    --secondary: #ff00ea;  /* Magenta */
    --accent: #ffed4e;     /* Yellow */
    --dark: #0a0e27;       /* Dark blue */
    --light: #e0f4ff;      /* Light cyan */
}
```

## 🚀 Deployment to Vercel

### Method 1: Using Vercel CLI (Recommended)

1. Install Vercel CLI globally:
```bash
npm install -g vercel
```

2. Navigate to your project directory:
```bash
cd your-project-folder
```

3. Deploy:
```bash
vercel
```

4. Follow the prompts. For production deployment:
```bash
vercel --prod
```

### Method 2: Using Vercel Dashboard

1. Go to [vercel.com](https://vercel.com) and sign in
2. Click "Add New Project"
3. Import your Git repository (or drag and drop the project folder)
4. Vercel will auto-detect the settings
5. Click "Deploy"

### Method 3: Deploy from GitHub

1. Push your code to a GitHub repository
2. Go to [vercel.com](https://vercel.com)
3. Click "Import Project"
4. Select your repository
5. Vercel will automatically deploy

## 📁 Project Structure

```
vr-resume/
├── index.html          # Main file with all code
├── vercel.json        # Vercel configuration
├── package.json       # Project metadata
└── README.md          # This file
```

## 🎮 How to Use

1. **Start**: Click "Enter the World" to begin
2. **Navigate**: Drag anywhere to rotate the camera view
3. **Explore**: Click on the glowing orbs to read about different aspects
4. **Close**: Click the × button to close info panels

## 💡 Tips for Best Results

- **Test Locally**: Open `index.html` in a modern browser (Chrome, Firefox, Edge)
- **Mobile**: The experience works on mobile but desktop is recommended
- **Performance**: The app is optimized for smooth 60fps rendering
- **Customization**: Don't be afraid to change colors, positions, and content
- **Add More Zones**: You can add as many zones as you want by adding objects to the `resumeData.zones` array

## 🔧 Technical Details

- **Framework**: Three.js r128
- **No Build Step**: Pure HTML/CSS/JS
- **CDN**: Three.js loaded from CloudFlare CDN
- **Rendering**: WebGL with antialiasing
- **Shadows**: PCF soft shadows enabled
- **Responsive**: Adapts to window resize

## 🌟 Advanced Customization

### Adding New Zones

1. Add a new object to `resumeData.zones`:
```javascript
{
    name: "Certifications",
    icon: "📜",
    color: 0xff9500,  // Orange
    position: [-5, 6, -5],  // x, y, z coordinates
    content: {
        title: "Professional Certifications",
        sections: [
            {
                heading: "AWS Solutions Architect",
                details: "Amazon Web Services • 2023"
            }
        ]
    }
}
```

2. The zone will automatically appear in the 3D world!

### Changing Zone Positions

Zones are positioned using `[x, y, z]` coordinates:
- `x`: Left (-) to Right (+)
- `y`: Down (-) to Up (+)
- `z`: Back (-) to Front (+)

Example: `[-8, 2, 0]` means 8 units left, 2 units up, at center depth

### Modifying Animations

Find the `animate()` function to adjust:
- Rotation speeds
- Float animation intensity
- Particle movement
- Camera behavior

## 📱 Browser Compatibility

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Edge 90+
- ✅ Safari 14+
- ⚠️ IE11: Not supported

## 🐛 Troubleshooting

**Black screen?**
- Check browser console for errors
- Ensure Three.js CDN is accessible
- Try a different browser

**Performance issues?**
- Reduce the number of stars in `createStarfield()`
- Lower the particle count in `createParticles()`

**Zones not appearing?**
- Check your `resumeData.zones` array
- Verify position coordinates aren't too far from camera
- Check browser console for errors

## 📄 License

MIT License - Feel free to use this for your own resume!

## 🤝 Credits

Created with Three.js and a passion for immersive experiences.

---

**Made with ❤️ and WebGL**

For questions or improvements, feel free to reach out!

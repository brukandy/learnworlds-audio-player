# 🎵 LearnWorlds Mobile Audio Player

Beautiful mobile-first audio player with dynamic color extraction from thumbnails. Perfect for LearnWorlds courses.

![Mobile Audio Player](https://img.shields.io/badge/LearnWorlds-Compatible-blue)

## ✨ Features

- 📱 **Mobile-first design** - Optimized for mobile devices
- 🎨 **Dynamic color extraction** - Background gradient adapts to thumbnail colors
- ⏯️ **Full playback controls** - Play/Pause, Rewind 10s, Forward 10s
- 📊 **Progress bar** - Interactive seek functionality
- 🖼️ **Circular thumbnails** - Beautiful circular image display
- 🎯 **Easy to embed** - Works seamlessly in LearnWorlds

## 🚀 Quick Start

### 1. Add your audio files
Place your MP3 files in the `/audio` folder

### 2. Add your thumbnails
Place your images in the `/thumbnails` folder

### 3. Update index.html
```html
<div class="mobile-audio-player"
     data-audio-src="./audio/your-track.mp3"
     data-title="Your Track Title"
     data-subtitle="Author Name"
     data-thumbnail="./thumbnails/your-image.jpg">
</div>
```

## 📁 Project Structure

```
learnworlds-audio-player/
├── index.html          # Main player file
├── audio/             # Your audio files (.mp3)
├── thumbnails/        # Your thumbnail images
└── README.md          # This file
```

## 🔧 How to Use

### Multiple Players
You can add multiple players on the same page:

```html
<div class="mobile-audio-player"
     data-audio-src="./audio/meditation-1.mp3"
     data-title="Morning Meditation"
     data-subtitle="Vishen"
     data-thumbnail="./thumbnails/morning.jpg">
</div>

<div class="mobile-audio-player"
     data-audio-src="./audio/meditation-2.mp3"
     data-title="Evening Meditation"
     data-subtitle="Vishen"
     data-thumbnail="./thumbnails/evening.jpg">
</div>
```

### Embed in LearnWorlds

1. Copy the entire HTML code from `index.html`
2. Go to LearnWorlds → Course → Add Section → Custom Code
3. Paste the code
4. Make sure your audio files are hosted (GitHub Pages, Cloudinary, etc.)

## 🌐 GitHub Pages Setup

1. Push to GitHub:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/learnworlds-audio-player.git
git push -u origin main
```

2. Enable GitHub Pages:
   - Go to Settings → Pages
   - Source: Deploy from branch `main`
   - Folder: `/ (root)`

3. Your player will be available at:
   `https://YOUR_USERNAME.github.io/learnworlds-audio-player/`

## 🎨 Customization

### Change Colors
Edit the CSS variables in `index.html`:
```css
--dominant-color: rgb(30, 58, 138); /* Default blue */
```

### Adjust Thumbnail Size
```css
.mobile-audio-thumbnail {
    width: 240px;  /* Change this */
    height: 240px; /* Change this */
}
```

## 📝 Data Attributes

| Attribute | Required | Description |
|-----------|----------|-------------|
| `data-audio-src` | ✅ | URL to audio file (.mp3) |
| `data-title` | ✅ | Track title |
| `data-subtitle` | ❌ | Author/subtitle |
| `data-thumbnail` | ✅ | URL to thumbnail image |

## 🐛 Troubleshooting

### Audio not playing
- Check console for CORS errors
- Ensure audio URL is accessible
- Use HTTPS URLs for production

### Color extraction not working
- Thumbnail must support CORS
- Image must be loaded before extraction
- Use `crossorigin="anonymous"` attribute

## 📄 License

MIT License - Feel free to use in your projects!

## 🙋 Support

For issues or questions, open an issue on GitHub.

---

Made with ❤️ for LearnWorlds

# Video Background Setup Instructions

## How to Add Your Hand-in-Water Video

### Step 1: Prepare Your Video File

1. **Video Requirements:**
   - Format: MP4 (H.264 codec) and WebM for best browser compatibility
   - Resolution: 1920x1080 (Full HD) or higher
   - File size: Keep under 5MB for faster loading (compress if needed)
   - Duration: 10-30 seconds (it will loop automatically)
   - Content: Hand in water footage symbolizing "living water"

2. **Compress Your Video (Optional but Recommended):**
   - Use tools like [HandBrake](https://handbrake.fr/) or [FFmpeg](https://ffmpeg.org/)
   - Reduce quality slightly to decrease file size
   - Target bitrate: 1-2 Mbps for web use

### Step 2: Create Video Folder

In your repository root, create a `videos` folder:

```bash
mkdir videos
```

### Step 3: Add Your Video Files

Place your video files in the `videos` folder with these names:
- `hand-in-water.mp4` (primary format)
- `hand-in-water.webm` (optional, for better browser support)

### Step 4: Update index.html

The video element is already set up in `index.html`. Simply uncomment these lines:

```html
<!-- Current (commented out): -->
<!-- <source src="videos/hand-in-water.mp4" type="video/mp4">
<source src="videos/hand-in-water.webm" type="video/webm"> -->

<!-- Change to (uncommented): -->
<source src="videos/hand-in-water.mp4" type="video/mp4">
<source src="videos/hand-in-water.webm" type="video/webm">
```

### Step 5: Test Your Video

1. Open `index.html` in a web browser
2. The video should autoplay, loop, and be muted
3. If the video doesn't load, the poster image (fallback) will show

## Alternative: Use a Video URL

If you're hosting the video elsewhere (like YouTube, Vimeo, or a CDN):

### For Direct Video URL:
```html
<source src="https://your-cdn.com/hand-in-water.mp4" type="video/mp4">
```

### For YouTube (requires different approach):
Note: YouTube doesn't support background video autoplay. Consider using a direct video file instead.

## Fallback Options

### Current Fallback (Animated CSS):
The site currently uses an animated CSS water effect as a fallback when no video is present. This provides a nice visual without requiring a video file.

### Poster Image Fallback:
The `poster` attribute on the `<video>` tag shows an image while the video loads or if it fails. The current poster is an inline SVG that matches the animated background.

### To Use a Custom Poster Image:
1. Add your image to an `images` folder
2. Update the poster attribute:
```html
<video class="hero-video" ... poster="images/hand-in-water-poster.jpg">
```

## Recommended Video

### Perfect Video Found!

**Video:** Slow Motion Close-Up of Washing Hands  
**By:** Andrew Schwark from Pexels  
**URL:** https://www.pexels.com/video/slow-motion-close-up-of-washing-hands-34762374/  
**License:** Free to use (Pexels License)  
**Why it's perfect:** Beautiful slow-motion footage of hands in water, symbolizing the "living water" theme

### How to Download This Video:

1. **Visit the video page:**
   - Go to: https://www.pexels.com/video/slow-motion-close-up-of-washing-hands-34762374/

2. **Download the video:**
   - Click the "Free Download" button
   - Choose quality: **HD 1920x1080** (recommended for best quality)
   - Or **HD 1280x720** (smaller file size, faster loading)

3. **Save the file:**
   - Save as `hand-in-water.mp4` in the `videos` folder
   - Location: `videos/hand-in-water.mp4`

4. **Uncomment the video source:**
   - Open `index.html`
   - Find the commented video source lines
   - Remove the `<!--` and `-->` comments

### License & Attribution

**Pexels License** allows you to:
- ✅ Use for commercial projects
- ✅ Use without attribution (though attribution is appreciated)
- ✅ Modify and edit the video

**Optional Attribution** (recommended for good practice):
Add to your footer or about page:
> "Hero video by Andrew Schwark from Pexels"

### Alternative Video Sources

If you prefer different footage:

1. **Free Stock Video Sites:**
   - [Pexels Videos](https://www.pexels.com/videos/) - Free, no attribution required
   - [Pixabay Videos](https://pixabay.com/videos/) - Free, no attribution required
   - [Videvo](https://www.videvo.net/) - Free and premium options
   - [Coverr](https://coverr.co/) - Free, no attribution required

2. **Search Terms:**
   - "hand in water"
   - "hand touching water"
   - "water ripples"
   - "hand cupping water"
   - "flowing water hand"

### Creating Your Own Video:
You can also film your own hand-in-water footage with a smartphone in good lighting.

## Troubleshooting

### Video Not Playing:

1. **Check file path:** Ensure the video file is in the correct location
2. **Check file format:** MP4 with H.264 codec is most compatible
3. **Check file size:** Very large files may not load on mobile
4. **Browser console:** Open developer tools (F12) to check for errors

### Video Not Autoplay on Mobile:

Mobile browsers often restrict autoplay with sound. Since the video is muted (`muted` attribute), it should autoplay. If it doesn't:
- Ensure the `muted` and `playsinline` attributes are present
- Some mobile browsers may still block autoplay - the poster image will show instead

### Performance Issues:

If the video causes performance issues:
1. Reduce video file size by compressing
2. Lower the resolution to 1280x720
3. Use the CSS animated background instead (current fallback)

## Git Considerations

### Adding Video to Git:

⚠️ **Warning:** Large video files can bloat your Git repository.

**Option 1: Add to Git (for small videos < 5MB):**
```bash
git add videos/hand-in-water.mp4
git commit -m "Add hero background video"
git push
```

**Option 2: Use .gitignore (recommended for large videos):**
Add to `.gitignore`:
```
videos/
```

Then host the video on a CDN or web hosting service and use the URL in the `src` attribute.

**Option 3: Git LFS (for large files):**
Use [Git Large File Storage](https://git-lfs.github.com/) to manage large video files efficiently.

## Current Setup

Without a video file present, the site uses:
1. **Primary:** Animated CSS water effect with gradient background
2. **Poster:** Inline SVG fallback image
3. **HTML5 Video Element:** Ready to accept video sources when you add them

The site is fully functional with the CSS animation and will seamlessly upgrade to use the video once you add the video files.

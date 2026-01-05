# 🗺️ Calgary Interactive Communities Map

An interactive, clickable map of Calgary communities built for real estate professionals. Click any community to view properties and listings in that area.

## 🚀 Live Demo

Once deployed, your map will be available at:
```
https://YOUR-USERNAME.github.io/calgary-map/
```

Or with a custom domain:
```
https://map.duikerproperties.com
```

## 📁 Files Included

- `index.html` - The interactive map webpage
- `CITY_OF_CALGARY_MAP_2025.svg` - The Calgary map SVG file
- `README.md` - This file with setup instructions

## 🛠️ Setup Instructions

### Option 1: Quick Setup (5 minutes)

1. **Create a GitHub account** (if you don't have one)
   - Go to https://github.com
   - Sign up for free

2. **Create a new repository**
   - Click the `+` icon in the top right
   - Select "New repository"
   - Name it: `calgary-map` (or any name you prefer)
   - Make it **Public**
   - Click "Create repository"

3. **Upload files**
   - Click "uploading an existing file"
   - Drag and drop BOTH files:
     - `index.html`
     - `CITY_OF_CALGARY_MAP_2025.svg`
   - Click "Commit changes"

4. **Enable GitHub Pages**
   - Go to repository Settings
   - Scroll to "Pages" in the left sidebar
   - Under "Source", select `main` branch
   - Click "Save"
   - Wait 2-3 minutes for deployment

5. **Get your URL**
   - Your map will be live at: `https://YOUR-USERNAME.github.io/calgary-map/`

### Option 2: Using GitHub Desktop (Easier for future updates)

1. **Download GitHub Desktop**
   - https://desktop.github.com/

2. **Create repository**
   - File → New Repository
   - Name: `calgary-map`
   - Local Path: Choose where to save
   - Click "Create Repository"

3. **Add files**
   - Copy both files into the repository folder
   - GitHub Desktop will show them as changes

4. **Publish**
   - Click "Publish repository"
   - Uncheck "Keep this code private"
   - Click "Publish repository"

5. **Enable Pages** (same as Option 1, step 4)

## 🔧 Customization

### Update Community URLs

Edit `index.html` and find the `communityURLs` object (around line 176):

```javascript
const communityURLs = {
    // Your Southeast Communities
    'Mahogany': 'https://duikerproperties.com/communities/mahogany',
    'Seton': 'https://duikerproperties.com/communities/seton',
    'Auburn Bay': 'https://duikerproperties.com/communities/auburn-bay',
    'Cranston': 'https://duikerproperties.com/communities/cranston',
    'Chestermere': 'https://duikerproperties.com/communities/chestermere',
    
    // Add more communities here
    'Community Name': 'https://your-url.com/community-page',
    
    // Default URL for unmapped communities
    'default': 'https://duikerproperties.com/communities'
};
```

### Change Colors/Styling

The map uses a purple gradient. To change colors, edit the CSS in `index.html`:

```css
/* Main gradient background */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Hover color for communities */
stroke: #3182ce;  /* Blue - change to any color */
```

### Add Google Analytics

Add before the closing `</head>` tag in `index.html`:

```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

## 🌐 Custom Domain Setup

### Using a Subdomain (Recommended)

1. **In your domain registrar** (GoDaddy, Namecheap, etc):
   - Add a CNAME record:
   - Name: `map` (or `calgary-map`)
   - Value: `YOUR-USERNAME.github.io`

2. **In GitHub repository settings**:
   - Go to Pages settings
   - Enter custom domain: `map.duikerproperties.com`
   - Click "Save"
   - Enable "Enforce HTTPS"

3. **Wait 24 hours** for DNS to propagate

### Result:
Your map will be at: `https://map.duikerproperties.com`

## 🔗 Embedding in Bold Trail

### Option 1: iFrame Embed
Add this to any Bold Trail page:

```html
<iframe 
    src="https://YOUR-USERNAME.github.io/calgary-map/" 
    width="100%" 
    height="800px" 
    frameborder="0"
    style="border-radius: 10px;"
></iframe>
```

### Option 2: Direct Link Button
Add a prominent button on your site:

```html
<a href="https://map.duikerproperties.com" 
   target="_blank"
   style="display: inline-block; padding: 15px 30px; background: #667eea; color: white; border-radius: 8px; text-decoration: none; font-weight: bold;">
   🗺️ Explore Calgary Communities Map
</a>
```

## 🎨 Branding with Royal LePage

To match Royal LePage colors, update these values in `index.html`:

```css
/* Royal LePage Gold: #C5A572 */
/* Royal LePage Blue: #003A70 */

background: linear-gradient(135deg, #003A70 0%, #C5A572 100%);
```

## 📱 Features

- ✅ Fully responsive (works on mobile, tablet, desktop)
- ✅ Zoom controls (+ / - buttons)
- ✅ Hover tooltips showing community names
- ✅ Click to view community details
- ✅ Links to your listing pages
- ✅ Smooth animations and transitions
- ✅ SEO optimized with meta tags
- ✅ Fast loading (hosted on GitHub's CDN)

## 🔄 Updating the Map

### To add new communities:
1. Edit `index.html`
2. Add community to `communityURLs` object
3. Commit and push changes
4. GitHub Pages auto-updates in 1-2 minutes

### To update the map graphic:
1. Replace `CITY_OF_CALGARY_MAP_2025.svg` with new file
2. Keep the same filename
3. Commit and push
4. Changes live in 1-2 minutes

## 📊 Tracking

The map includes click tracking. If you add Google Analytics (see above), you'll see:
- Which communities people click
- How often each community is viewed
- User navigation patterns

Event name: `community_click`
Parameters:
- `community_name`: The community clicked
- `destination_url`: Where they were sent

## 🆘 Support & Issues

Common issues:

**Map not showing:**
- Check that BOTH files are uploaded
- Files must be in the same folder
- Wait 2-3 minutes after enabling Pages

**Custom domain not working:**
- DNS can take up to 24 hours
- Verify CNAME record is correct
- Check GitHub Pages settings

**Communities not clickable:**
- Make sure SVG file loaded correctly
- Check browser console for errors
- Try hard refresh (Ctrl+Shift+R)

## 📞 Contact

Built for Kyle Duiker | Duiker Properties
Royal LePage Solutions | Calgary, AB

- Website: https://duikerproperties.com
- Map Repository: https://github.com/YOUR-USERNAME/calgary-map

## 📄 License

Free to use and modify for your real estate business.

---

**Pro Tip:** After setting up, test all your community links to ensure they point to the correct pages on your website!

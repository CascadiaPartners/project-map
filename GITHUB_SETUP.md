# Quick Start Guide - GitHub Setup

## Step 1: Create GitHub Repository

1. Go to https://github.com/new
2. Name your repository (e.g., "project-map")
3. Choose "Public" visibility
4. Do NOT initialize with README (we already have one)
5. Click "Create repository"

## Step 2: Upload Files to GitHub

### Option A: Using GitHub Web Interface
1. On your new repository page, click "uploading an existing file"
2. Drag and drop ALL files and folders from the project-map folder
3. Write a commit message: "Initial commit"
4. Click "Commit changes"

### Option B: Using Git Command Line
```bash
# Navigate to your project folder
cd project-map

# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit"

# Add remote repository (replace with your GitHub URL)
git remote add origin https://github.com/yourusername/project-map.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" tab
3. Click "Pages" in the left sidebar
4. Under "Source", select "GitHub Actions"
5. The workflow will automatically deploy your site

## Step 4: Add Your Data

1. Replace the sample data in `data/Projects_0.js` with your actual project data
2. Make sure your GeoJSON follows the same format:
   - Each feature must have ProjectName, Location, and ProjectType properties
   - ProjectType must be one of the 5 defined categories
   - Coordinates are in [longitude, latitude] format

## Step 5: View Your Map

After a few minutes, your map will be live at:
```
https://yourusername.github.io/project-map/
```

## Troubleshooting

**Map doesn't load:**
- Check browser console for errors (F12)
- Verify Projects_0.js is valid JavaScript
- Ensure all coordinates are valid numbers

**GitHub Pages not working:**
- Wait 2-5 minutes after enabling Pages
- Check the Actions tab for deployment status
- Verify the repository is public

**Markers not showing:**
- Verify your coordinates are in correct format: [longitude, latitude]
- Check that ProjectType matches one of the 5 defined types exactly

## Customization

Edit `index.html` to:
- Change colors in the `style_Projects_0_0` function
- Modify marker sizes (radius property)
- Update map bounds and zoom levels
- Change the basemap style

## Support

For issues or questions:
1. Check the README.md for detailed documentation
2. Review Leaflet.js documentation: https://leafletjs.com/
3. Open an issue on GitHub

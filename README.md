# Project Map

An interactive map visualization displaying various urban development and planning projects across the United States.

## Features

- **Interactive Map**: Built with Leaflet.js for smooth navigation and exploration
- **Project Categories**: Five distinct project types with color-coded markers:
  - 🟣 P3s & Development Offerings
  - 🟢 Real Estate & Development
  - 🔵 Strategic Planning & Urban Design
  - 🟠 Urban Analytics
  - 🔴 Zoning & Policy Analysis
- **Cluster Markers**: Automatically groups nearby markers for better visualization
- **Popup Information**: Click on any marker to view project details

## Demo

View the live map: [GitHub Pages URL will be here after deployment]

## Project Structure

```
project-map/
├── index.html              # Main HTML file
├── data/
│   └── Projects_0.js       # GeoJSON data file with project locations
├── README.md               # This file
└── LICENSE                 # License file (optional)
```

## Setup

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/yourusername/project-map.git
cd project-map
```

2. Open `index.html` in a web browser or use a local server:
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js
npx serve

# Using PHP
php -S localhost:8000
```

3. Navigate to `http://localhost:8000` in your browser

### GitHub Pages Deployment

1. Push your code to GitHub:
```bash
git add .
git commit -m "Initial commit"
git push origin main
```

2. Enable GitHub Pages:
   - Go to your repository settings
   - Navigate to "Pages" section
   - Select "main" branch as source
   - Save

3. Your map will be available at: `https://yourusername.github.io/project-map/`

## Adding Your Own Data

Replace the contents of `data/Projects_0.js` with your own GeoJSON data. The file should follow this structure:

```javascript
var json_Projects_0 = {
  "type": "FeatureCollection",
  "name": "Projects_0",
  "crs": { "type": "name", "properties": { "name": "urn:ogc:def:crs:OGC:1.3:CRS84" } },
  "features": [
    {
      "type": "Feature",
      "properties": {
        "ProjectName": "Your Project Name",
        "Location": "City, State",
        "ProjectType": "Urban Analytics"  // Must match one of the 5 types
      },
      "geometry": {
        "type": "Point",
        "coordinates": [ longitude, latitude ]
      }
    }
    // Add more features here
  ]
}
```

## Technologies Used

- **Leaflet.js** (v1.9.4): Open-source JavaScript library for interactive maps
- **Leaflet.markercluster**: Plugin for clustering markers
- **Autolinker**: Automatically converts URLs in text to clickable links
- **Stamen Toner basemap**: High-contrast black and white map tiles

## Customization

### Changing Colors

Edit the `style_Projects_0_0` function in `index.html` to modify marker colors:

```javascript
fillColor: 'rgba(141,40,208,1.0)',  // Purple for P3s & Development Offerings
```

### Modifying Marker Size

Change the `radius` property in the style function:

```javascript
radius: 7.2,  // Adjust this value
```

### Updating the Map Bounds

Modify the `fitBounds` coordinates to focus on a different area:

```javascript
.fitBounds([[minLat, minLon], [maxLat, maxLon]]);
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

This project is open source and available under the [MIT License](LICENSE).

## Credits

- Map interface generated using [qgis2web](https://github.com/tomchadwin/qgis2web)
- Basemap tiles by [Stadia Maps](https://www.stadiamaps.com/)
- Original Stamen Design

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

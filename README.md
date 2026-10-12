# Coimbatore Surface Change Explorer (2018–2025)

Ready-to-publish static website for a Sentinel-2 Bare Soil Index analysis.

## Publish
1. Create a public GitHub repository, e.g. `coimbatore-bsi-explorer`.
2. Upload **everything inside this folder** to the repository root. `index.html`, `style.css`, `script.js`, and `assets/` must remain together.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, then select `main` and `/(root)`, and save.
5. Wait for deployment. GitHub shows the public URL in Pages settings.

## Included
- Responsive research page
- Interactive annual mean BSI chart
- Difference-map screenshot from the analysis
- Downloadable CSV of annual mean values
- Methodology, interpretation, limitations, and dataset links

The chart loads Chart.js from jsDelivr, so it needs an internet connection. The difference map is a static image, not a live raster layer.

## Method
Dataset: `COPERNICUS/S2_SR_HARMONIZED` in Google Earth Engine. Seasonal window: January 1 to April 1 each year. BSI = ((B11 + B4) − (B8 + B2)) / ((B11 + B4) + (B8 + B2)). Difference = BSI(2025) − BSI(2018), using pixels with at least one valid observation in both endpoint years.

Interpretation caution: BSI is a spectral index, not a direct measurement of bare-soil area. The common mask does not equalize observation counts or acquisition dates. Verify and cite the boundary source/vintage in the submitted report.

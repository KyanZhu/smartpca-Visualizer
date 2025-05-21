# PCA Visualization Tool for Population Genetics

This is an interactive web-based visualization tool for exploring Principal Component Analysis (PCA) results in population genetics studies. The tool allows researchers and analysts to upload PCA results in .evec format and interactively explore the genetic relationships between populations.

## Features

- **Interactive Visualization**: Zoom, pan, and hover over data points to view detailed information
- **Population Filtering**: Show/hide specific populations or search for populations of interest
- **Responsive Design**: Works on various screen sizes and devices
- **Export Options**: Save visualizations as SVG or PNG files
- **Customizable Legend**: Click on legend items to toggle population visibility

## Usage

### Online Version

1. Open [smartpca-Visualizer](https://kyanzhu.github.io/smartpca-Visualizer/)
2. Upload your .evec format file using the "Upload custom data" button
3. Interact with the visualization using mouse controls:
   - Scroll to zoom
   - Drag to pan
   - Hover over points for detailed information

### Local Installation

1. Clone this repository:
   ```
   git clone https://github.com/KyanZhu/smartpca-Visualizer.git
   ```
2. Navigate to the project directory:
   ```
   cd smartpca-Visualizer
   ```
3. Open `pca_visualization.html` in your web browser

## File Format

The tool accepts files in the `.evec` format, a standard output format from EIGENSOFT's smartpca. The expected format is:

```
#EIGENVALUES: 0.123 0.045 0.022 ...
Sample1 0.0054 0.0021 0.0032 ... Population1
Sample2 0.0067 -0.0043 0.0021 ... Population2
...
```

Where:
- First line contains eigenvalues (optional, will be skipped)
- Each subsequent line contains:
  - Sample ID
  - PC1 value, PC2 value, etc.
  - Population name (last column)

## Technical Details

This tool uses:
- D3.js for data visualization
- FileSaver.js for exporting visualizations
- No server-side processing required - all processing happens in your browser

## Screenshots
 ![](https://github.com/KyanZhu/smartpca-Visualizer/blob/main/screenshot.png?raw=true)

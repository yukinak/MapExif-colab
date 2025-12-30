![License](https://img.shields.io/badge/License-MIT-green)
![Python](https://img.shields.io/badge/Python-3.8-orange)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yukinak/MapExif-colab/blob/main/MapEXIF_colab.ipynb)


# MapEXIF-Colab
This repository provides a Google Colab notebook to read EXIF data (including GPS information) from images stored in a specific folder (e.g., on Google Drive) and visualize them on a map.

![Demo Image](demo_image.png)

## Features
- Extract EXIF metadata (latitude, longitude) from HEIC, HEIF, JPEG, PNG, and TIFF images.
- Convert GPS coordinates from DMS (Degree/Minute/Second) to decimal format.
- Visualize locations on an interactive map using **[Folium](https://python-visualization.github.io/folium/latest/)**.
- Compatible with Google Colab + Google Drive workflow.

## Requirements
The notebook installs necessary libraries automatically, but the core dependencies are:

```bash
pip install exifread
pip install folium
```

## Usage
1. Open the notebook `MapEXIF_colab.ipynb` in **Google Colab**.
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yukinak/MapExif-colab/blob/main/MapEXIF_colab.ipynb)

2. Mount Google Drive:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```
3. Place your images (HEIC/HEIF/JPEG/PNG/TIFF) in a target folder inside your Drive.
4. Update the `img_directory` path in the notebook to match your image folder.
5. Run all cells.  
6. Visualize the extracted coordinates on an interactive map using **folium**.

## Example Output
- Console log of file names with GPS.
- Interactive map with markers at photo locations.

## File Structure
```
├── MapEXIF_colab.ipynb   # Main notebook
├── README.md             # This file
```

## Notes
- Works with HEIC, HEIF, JPEG, PNG, and TIFF images containing GPS EXIF metadata.
- If an image lacks GPS information, it will be skipped with a warning message.

## License
MIT License

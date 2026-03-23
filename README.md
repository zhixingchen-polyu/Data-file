# Data-file
Data + Code availability

import os
from datetime import datetime

def generate_readme():
    """Generate README.md with data and code availability."""
    
    readme_content = """# Infrastructure Diversity Analysis – Data & Code Availability

This repository contains the code and associated data sources used for the analysis of infrastructure diversity. All datasets and scripts are publicly accessible, ensuring full reproducibility of the results presented in the associated study.

---

## Data availability

The following datasets were used in this study. Each source is openly available and properly cited below.

### Building footprint data
- **Global building footprints** (excluding China)  
  Microsoft Global ML Building Footprints  
  [https://github.com/microsoft/GlobalMLBuildingFootprints](https://github.com/microsoft/GlobalMLBuildingFootprints)

- **China building footprints**  
  CBRA and CMAB datasets  
  [https://zenodo.org/records/7500612](https://zenodo.org/records/7500612)  
  [https://doi.org/10.6084/m9.figshare.27992417.v2](https://doi.org/10.6084/m9.figshare.27992417.v2)

### Impervious surface data
Star Cloud Data Service Platform  
[https://data-starcloud.pcl.ac.cn/iearthdata](https://data-starcloud.pcl.ac.cn/iearthdata)

### Satellite imagery
Google Earth satellite imagery  
Google Earth API  
[https://www.google.com/earth](https://www.google.com/earth)

### Human settlement boundaries
Global Human Settlement Layer (GHSL)  
European Commission, Joint Research Centre  
[https://human-settlement.emergency.copernicus.eu/datasets.php](https://human-settlement.emergency.copernicus.eu/datasets.php)

### POI, AOI, and land use data
OpenStreetMap (OSM) community  
[https://www.openstreetmap.org](https://www.openstreetmap.org)  
OSM shapefile documentation:  
[https://download.geofabrik.de/osm-data-in-gis-formats-free.pdf](https://download.geofabrik.de/osm-data-in-gis-formats-free.pdf)

### Socioeconomic data
- **Grid-level per capita GDP** (PPP, 1990–2022)  
  Downscaled gridded global GDP dataset  
  [https://zenodo.org/records/16741980](https://zenodo.org/records/16741980)

- **Grid-level population**  
  LandScan Global Population Database  
  [https://landscan.ornl.gov](https://landscan.ornl.gov)

- **Human Development Index (HDI)**  
  United Nations Development Programme  
  [https://hdr.undp.org](https://hdr.undp.org)

---

## Code availability

All code used for data processing, analysis, and figure generation is publicly available in this repository:

[https://github.com/RCAIG/Infrastructure_diversity](https://github.com/RCAIG/Infrastructure_diversity)

Scripts are organized by analytical step and include detailed comments to support reproducibility.

---

## License

Please refer to the original data sources and the repository for respective licensing terms.

---

*README generated on {date}*
""".format(date=datetime.now().strftime("%Y-%m-%d"))

    # Write to file
    with open("README.md", "w", encoding="utf-8") as f:
        f.write(readme_content)
    
    print("README.md generated successfully.")

if __name__ == "__main__":
    generate_readme()

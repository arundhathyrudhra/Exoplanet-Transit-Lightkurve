# Exoplanet Transit Detection using Lightkurve

This project demonstrates the detection and analysis of exoplanets using transit photometry from NASA’s Kepler mission data. The workflow is implemented using Python and the Lightkurve package in a cloud-based environment (Google Colab).

---

## Project Overview

The goal of this project is to analyze stellar light curves and detect exoplanets using the transit method. The complete pipeline includes:

- Extracting light curves from Kepler Target Pixel Files (TPF)
- Removing noise and trends (detrending)
- Detecting periodic signals using the Box Least Squares (BLS) algorithm
- Phase folding the light curve to reveal transits
- Estimating planetary parameters from transit features

---

## Systems Analyzed

### Kepler-10 System
- A relatively clean and stable light curve
- Ideal for demonstrating basic transit detection
- Clear periodic transit signal
- Used as a baseline system

### TRAPPIST-1 System
- A complex multi-planet system
- Short orbital periods (fast transits)
- Higher noise and multiple transit signatures
- Demonstrates robustness of the analysis pipeline

---

## Methodology

The workflow implemented in this project follows real astronomical data analysis techniques:

1. **Data Acquisition**
   - Kepler TPF data accessed using Lightkurve

2. **Light Curve Extraction**
   - Aperture photometry applied to obtain flux vs time

3. **Detrending**
   - Long-term noise removed using flattening techniques

4. **Transit Detection**
   - Box Least Squares (BLS) algorithm used to identify periodic signals

5. **Phase Folding**
   - Light curve folded to align all transit events

6. **Parameter Estimation**
   - Transit depth
   - Planet-to-star radius ratio (Rp/Rs)
   - Transit duration
   - Orbital period

---

## Results Summary

| Parameter            | Kepler-10        | TRAPPIST-1        |
|---------------------|------------------|-------------------|
| Orbital Period      | ~0.8 days        | ~1–3 days         |
| Transit Depth       | Larger           | Smaller           |
| Signal Clarity      | High             | Moderate          |
| System Complexity   | Single planet    | Multi-planet      |

---

## Key Insights

- Kepler-10 provides a clean and easily detectable transit signal.
- TRAPPIST-1 shows more complex behavior due to multiple planets.
- The pipeline successfully adapts to both simple and complex systems.
- Transit depth directly relates to planetary size.
- Shorter orbital periods lead to more frequent transit events.

---

## Tools and Technologies

- Python
- Lightkurve
- NumPy
- Matplotlib
- Google Colab (Cloud Computing)

---

## Project Structure
Exoplanet-Transit-Lightkurve/
│
├── notebooks/
│ ├── kepler10_analysis.ipynb
│ ├── trappist1_analysis.ipynb
│ └── comparison_analysis.ipynb
│
├── figures/
│ ├── kepler10_transit.png
│ ├── trappist1_transit.png
│ └── comparison_plot.png
│
├── data/
│ └── flattened_lightcurve.csv
│
├── README.md
├── requirements.txt
└── .gitignore

---

## Conclusion

This project successfully replicates real-world exoplanet detection techniques using open-source tools and publicly available space telescope data. By analyzing both a simple system (Kepler-10) and a complex system (TRAPPIST-1), the project demonstrates the flexibility and robustness of the transit detection pipeline.

---

## Future Improvements

- Analyze additional multi-planet systems
- Improve transit modeling (limb darkening effects)
- Automate detection for large datasets
- Apply machine learning for classification

---

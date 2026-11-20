# From Anomaly to Anticyclone
### Following Argo Float 1900857 Through the Agulhas Region

An independent oceanographic investigation combining Argo float observations, satellite altimetry, and mesoscale eddy tracking to examine anomalous intermediate-depth water properties in the Agulhas region of the Southern Ocean.

**Study period:** 2008–2013  
**Primary investigation:** May 2009–January 2010  
**Study region:** Southwestern Indian Ocean / Agulhas region  
**Argo float:** 1900857  
**Methods:** Python, oceanographic data analysis, satellite altimetry, geospatial analysis

## Project Overview

This project began with an unexpected observation in the hydrographic record of Argo float 1900857.

During cycle 44, on 13 May 2009, the float recorded exceptionally warm, saline water extending into intermediate depths. The anomaly was accompanied by a pronounced depression of potential-density surfaces relative to neighboring profiles.

The initial investigation raised a question:

**Could the anomalous hydrographic structure be explained by an encounter with an anticyclonic mesoscale eddy?**

To investigate this possibility, I combined in situ hydrographic measurements with satellite-derived sea-level anomalies and mesoscale eddy-tracking records.

Expanding the analysis to the complete float record revealed a second, more persistent anomaly during late 2009. This observation ultimately led to the identification of a satellite-tracked anticyclone and a quantitative assessment of the float's position relative to its effective boundary.

## Research Objectives

1. Identify and characterize unusual hydrographic observations in the Argo float record.
2. Examine temperature, salinity, and potential-density structure during anomalous profiles.
3. Evaluate potential relationships between hydrographic anomalies and mesoscale circulation.
4. Identify candidate anticyclonic eddies using satellite altimetry and eddy-tracking products.
5. Quantify the spatial relationship between the float and identified eddies.
6. Assess whether the available evidence supports an anticyclonic eddy encounter.

## Data Sources

### Argo Float Observations

**Float:** 1900857

Argo provides autonomous measurements of ocean temperature, salinity, pressure, and geographic position.

The analysis uses these observations to examine hydrographic variability, calculate seawater properties, and investigate changes in vertical density structure.

Source: [Argo International Program](https://argo.ucsd.edu/)

### Satellite Altimetry

Satellite-derived sea-level anomaly observations were used to investigate mesoscale circulation near the float.

The analysis includes satellite fields for 13 May 2009 and 19 November 2009.

**Data product:** Copernicus Marine DUACS gridded sea-level observations.

Source: [Copernicus Marine Service](https://marine.copernicus.eu/)

### Mesoscale Eddy Trajectory Atlas

The AVISO Mesoscale Eddy Trajectory Atlas (META4.0) was used to identify and track anticyclonic features.

The analysis incorporates eddy-center positions, effective radii, tracking identifiers, and satellite-derived effective contours.

Source: [AVISO+](https://www.aviso.altimetry.fr/)

## Methodology

### 1. Hydrographic Anomaly Detection

Temperature, salinity, and potential-density profiles were examined across the float record.

Anomalous observations were identified through changes in intermediate-depth salinity structure, hydrographic properties, and the vertical positions of selected isopycnals.

### 2. Density Structure Analysis

The pressure of the σ₀ = 27.0 kg/m³ isopycnal was calculated across the float record.

This provided a quantitative measure of changes in vertical density structure and helped identify intervals of unusually deep isopycnals.

### 3. Satellite Altimetry Investigation

Satellite sea-level anomaly fields were examined near anomalous float observations.

Positive sea-level anomalies were evaluated as potential indicators of anticyclonic mesoscale circulation.

### 4. Eddy Identification and Tracking

Candidate anticyclones were identified using the META4.0 atlas.

Tracking records were retrieved to reconstruct the movement and observational history of the selected eddy.

### 5. Float–Eddy Spatial Analysis

Float positions were matched with corresponding daily eddy observations.

Two complementary approaches were used:

- **Normalized proximity:** Geographic distance from the float to the eddy center divided by the eddy's effective radius.
- **Contour containment:** Geographic point-in-polygon tests using the satellite-derived effective contour.

The contour-based approach avoids assuming that mesoscale eddies have circular boundaries.

## Key Findings

### May 2009: An Extreme Hydrographic Anomaly

Argo cycle 44 exhibited exceptionally warm, saline intermediate-depth water.

At approximately 500 dbar:

| Property | Cycle 43 | Cycle 44 | Cycle 45 |
|---|---:|---:|---:|
| Conservative Temperature (°C) | 6.298 | 13.414 | 6.666 |
| Absolute Salinity (g/kg) | 34.553 | 35.445 | 34.579 |
| Potential Density σ₀ (kg/m³) | 27.034 | 26.524 | 27.006 |

Three examined isopycnals were depressed by approximately 316–406 dbar relative to neighboring-profile means.

The σ₀ = 27.0 kg/m³ isopycnal reached approximately 879 dbar, its deepest observed position in the float record.

Satellite observations identified a nearby positive sea-level anomaly and candidate anticyclone. However, the evidence was insufficient to confirm that the float was enclosed within the eddy.

### Late 2009: A Persistent Hydrographic Anomaly

A second period of unusually deep isopycnals was identified during cycles 60–68.

Eight of the ten deepest σ₀ = 27.0 observations in the 192-cycle record occurred within this interval.

The profiles also exhibited elevated intermediate-depth temperature and salinity, accompanied by relatively low potential density.

Unlike cycle 44, this anomaly persisted across multiple successive observations.

### Identification of a Tracked Anticyclone

Satellite observations for 19 November 2009 revealed a localized positive sea-level anomaly near cycle 63.

The corresponding META4.0 anticyclone was identified as:

| Attribute | Value |
|---|---|
| Track | 477593 |
| Segment | 10 |
| Type | Anticyclonic |
| First observation | 1 September 2009 |
| Last observation | 22 January 2010 |
| Daily observations | 144 |

The tracked feature persisted through the period of anomalous hydrographic observations.

### Float–Eddy Containment

Comparison of float positions with the anticyclone's effective contours produced the following results:

- **13 of 14** examined float positions were inside the corresponding eddy contours.
- Cycle 58 was the only examined observation outside the contour.
- **11 consecutive observed positions**, cycles 59–69, were inside the tracked eddy.
- These observations spanned approximately 100 days, from 10 October 2009 to 18 January 2010.

The results provide strong evidence of a sustained spatial association between the Argo float and the satellite-tracked anticyclone.

## Scientific Interpretation

The investigation supports an association between the late-2009 hydrographic anomaly and an anticyclonic mesoscale eddy.

The combination of warm, saline intermediate-depth waters, depressed isopycnals, satellite-derived sea-level anomalies, and repeated containment within an independently tracked anticyclone provides a consistent physical interpretation.

However, several limitations remain:

- Argo profiles were separated by approximately ten days.
- Satellite-derived effective contours represent surface mesoscale structures.
- Spatial containment does not independently demonstrate continuous subsurface trapping.
- The May 2009 anomaly cannot be conclusively attributed to a particular eddy.

The findings therefore support a sustained float–eddy association during late 2009 without establishing uninterrupted subsurface trapping.

## Tools and Technologies

**Programming and analysis**
- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- xarray

**Oceanographic calculations**
- TEOS-10 seawater thermodynamics
- Gibbs SeaWater (GSW) Oceanographic Toolbox

**Geospatial analysis**
- Geographic distance calculations
- Eddy trajectory matching
- Point-in-polygon containment testing

**Data access**
- argopy
- Copernicus Marine
- AVISO META4.0

## Project Structure

The project includes exploratory hydrographic analysis, satellite altimetry investigations, eddy-tracking calculations, and scientific visualizations.

The accompanying portfolio website presents the investigation as a chronological research narrative, from the initial anomaly through satellite-based validation.

## Reproducibility

The analysis uses publicly available oceanographic datasets.

Reproducing the results requires access to the corresponding Argo float profiles, satellite altimetry fields, and META4.0 eddy-tracking records.

The results depend on matching observations by date and geographic position, calculating seawater properties consistently, and distinguishing effective-radius proximity from actual contour containment.

## Project Status

**Exploratory investigation completed.**

The next phase will focus on a more detailed hydrographic analysis of water-mass properties and vertical structure during the identified anticyclonic encounter.

## Acknowledgments and Data Attribution

Argo data are collected and made freely available by the international Argo program and contributing national programs.

Satellite altimetry products are provided through the Copernicus Marine Service.

Mesoscale eddy tracking information is derived from the AVISO Mesoscale Eddy Trajectory Atlas (META4.0).

Users of the underlying datasets should follow the respective providers' citation and acknowledgment requirements.

---

*Independent marine geoscience research project developed using publicly available oceanographic observations.*

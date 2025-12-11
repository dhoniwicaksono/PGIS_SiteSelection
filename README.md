# Yogyakarta Strategic Urban Issues: Participatory Mapping Prototype

  

## 📖 Overview

This repository hosts a web-based **Participatory GIS (PGIS)** prototype designed to facilitate the collection of spatial data regarding strategic urban issues in the **Special Region of Yogyakarta (DIY)**.

Developing effective spatial plans (*Rencana Tata Ruang*) requires capturing the nuanced, ground-level perspectives of various stakeholders—from local government officials to business owners and community members. This tool bridges the gap between top-down planning and bottom-up aspirations, allowing users to digitize, attribute, and export specific urban issues or development preferences directly from a browser.

## 🎯 Purpose & Context

Urban planning in the Yogyakarta agglomeration area faces complex challenges involving rapid urbanization, heritage conservation, and service distribution. This tool was developed to:

1.  **Democratize Data Collection:** Provide a user-friendly interface for non-GIS experts to mark locations of interest.
2.  **Support Spatial Planning:** Gather crowdsourced data on strategic issues (e.g., congestion points, economic hubs, service gaps) to inform the *Peninjauan Kembali* (Review) or formulation of Spatial Plans.
3.  **Visual Verification:** Allow stakeholders to cross-reference their input against existing infrastructure layers (Education, Health, Government, and Economy).

## ✨ Key Features

  * **📍 Point-Based Data Collection:** Users can drop pins, categorize stakeholders, and input detailed reasoning for specific locations.
  * **📱 Mobile-First Responsive Design:** Fully optimized interface that adapts from desktop dashboards to mobile field surveys (including a tab-based navigation for small screens).
  * **🗺️ Rich Contextual Layers:**
      * **Government:** Hierarchy visualization (Provincial to Village level).
      * **Health:** Hospitals, Puskesmas, and Clinics.
      * **Education:** Schools (clustered for readability) and Universities.
      * **Economy:** Traditional and modern markets.
  * **🔍 Administrative Search:** Built-in autocomplete search for administrative boundaries within DIY (Provincial, Regency, District, Village).
  * **💾 Client-Side Export:** Privacy-focused and serverless capability to export collected points immediately to **CSV** and **GeoJSON** formats.
  * **📡 Multi-Basemap Support:** Toggle between OSM Standard, Esri Satellite, and Public Transport maps.

## 🛠️ Technology Stack

This project is built as a lightweight, static web application to ensure ease of deployment and accessibility.

  * **Core:** HTML5, CSS3, Vanilla JavaScript.
  * **Mapping Engine:** [Leaflet.js](https://leafletjs.com/) (v1.9.4).
  * **Clustering:** Leaflet.markercluster.
  * **Data Format:** GeoJSON for reference layers; CSV/GeoJSON for data export.

## 🚀 Getting Started

### Prerequisites

You do not need a backend server (Node.js, PHP, Python) to run this prototype. It runs entirely in the browser.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/jogja-participatory-mapping.git
    ```
2.  **Navigate to the folder:**
    ```bash
    cd jogja-participatory-mapping
    ```
3.  **Launch:**
    Open `index.html` in any modern web browser.

> **Note:** To ensure the AJAX requests for local GeoJSON files (in the `/data` folder) work correctly, it is recommended to run this via a local server (e.g., Live Server in VS Code) rather than opening the file directly via `file://` protocol, to avoid CORS policies.

## 📊 Data Schema

The application collects the following attributes for every point recorded:

| Field | Description |
| :--- | :--- |
| `respondent_id` | Unique identifier for the surveyor/stakeholder (e.g., R01). |
| `stakeholder_group` | Category (Govt, Business, Agency, etc.). |
| `mapping_object` | The specific issue or object being mapped. |
| `point_id` | Auto-generated ID for the spatial feature. |
| `latitude/longitude` | WGS84 coordinates. |
| `reason` | Qualitative description of the strategic issue. |
| `map_source` | Reference used (WebGIS, Printed Map, GPS). |

## 🤝 Contribution

Contributions are welcome\! If you are a planner, developer, or researcher interested in the Yogyakarta spatial planning context:

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/NewLayer`)
3.  Commit your Changes (`git commit -m 'Add new transport layer'`)
4.  Push to the Branch (`git push origin feature/NewLayer`)
5.  Open a Pull Request

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

-----

*This tool is a prototype developed for academic/planning research purposes in the Special Region of Yogyakarta.*

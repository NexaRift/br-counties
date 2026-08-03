# BR-Counties

`br-counties` is an open-data project that reorganizes Brazilian municipal demographic, territorial, and socioeconomic data into **Functional Counties**, based on the official regionalization framework established by the Brazilian Institute of Geography and Statistics (IBGE).

By aggregating municipal-level metrics into Immediate Geographic Regions (*Regiões Geográficas Imediatas*), this repository provides a consolidated spatial dataset designed for regional planning, spatial analysis, and public policy evaluation.

---

## Conceptual Framework & Motivation

Administrative divisions in Brazil often obscure functional urban dynamics. A single municipality may operate as an isolated unit on paper while functioning as the economic and service core for several surrounding towns in practice.

To capture these spatial interactions, IBGE established a regional hierarchy based on urban networks, daily population flows, and service accessibility. The `br-counties` project adopts this division to structure Brazilian territory into functional units equivalent to **Counties**:

### 1. Urban Concentrates and Population Arrangements
High-density urban cores and conurbations with populations exceeding 100,000 inhabitants. These arrangements exhibit strong integration between peripheral municipalities and the central nucleus through daily commuting, shared labor markets, and physical urban expansion.

### 2. Immediate Geographic Regions (RGIs) — The Functional Counties
RGIs are defined by immediate population needs, including access to retail, employment, primary and secondary healthcare, education, and basic public administration services (such as judicial courts and social security centers). In this project, each RGI is mapped as a **Functional County**, representing the primary operational scale of regional daily life.

### 3. Intermediate Geographic Regions (RGInts) — The Regional Macro-Structure
RGInts group multiple RGIs around higher-order urban centers (metropolises or regional capitals). They reflect complex economic functions, specialized public management flows, and regional infrastructure networks.

---

## Repository Structure

```text
br-counties/
├── data/                        # Standardized CSV datasets by state
│   ├── PR_Counties.csv
│   └── ...
├── docs/                        # MkDocs source files
│   ├── index.md                 # Project home page
│   ├── overview.md              # National territorial overview
│   └── brazil/                  # State-level documentation
│       ├── pr/                  # Paraná state
│       │   ├── index.md         # State overview and county index
│       │   ├── curitiba.md      # Curitiba county profile
│       │   └── ...
│       └── .../
├── .github/
│   └── workflows/
│       └── deploy.yml           # Automated GitHub Pages deployment
├── mkdocs.yml                   # MkDocs configuration
├── LICENSE
└── README.md
```

---

## Dataset Schema

The primary datasets are distributed in UTF-8 encoded `.csv` format under the `data/` directory. Each record corresponds to a municipality and its respective regional hierarchy, along with key physical and social metrics:

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `Cod_IBGE` | String | Unique 7-digit municipal code assigned by IBGE |
| `Municipio` | String | Official municipal name |
| `Regiao_Intermediaria` | String | Parent Intermediate Geographic Region |
| `Regiao_Imediata` | String | Immediate Geographic Region (Functional County) |
| `Populacao` | Integer | Total population (IBGE Census / Estimates) |
| `Area_km2` | Float | Territorial area in square kilometers |
| `Densidade_hab_km2` | Float | Calculated population density (inhabitants/km²) |
| `IDHM` | Float | Municipal Human Development Index (3 decimal places) |

---

## Documentation

The comprehensive regional encyclopedia — containing detailed county profiles, aggregated indicators, and regional synthesis — is maintained in Portuguese on the project's website:

* [BR-Counties Documentation](https://NexaRift.github.io/br-counties/)

---

## Licensing

This project is open-source and available under the terms of the **MIT License**. You are free to use, modify, and distribute the data for both academic, personal, and commercial purposes, provided proper attribution is maintained.
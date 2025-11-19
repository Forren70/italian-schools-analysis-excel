# 🇮🇹 Italian Schools Analysis Project (2025)

---

## 📊 Data Source Overview

The analysis is based on the following initial file:

**File:** `School_Analysis.xlsx`

This file contains information for **51,091 public schools in Italy** for the academic year 2025/2026. The Excel file is structured across **4 sheets**: `scuole`, `tipologie`, `comuni`, and `province`.

### Origin and Adaptation
The data was adapted and simplified from the original CSV file:
`SCUANAGRAFESTAT20252620250901.csv`

The source data is openly published by the Ministry of Education (MIUR).

**Source Link:** [Dati Istruzione (MIUR) - Distribuzione 2025/2026](https://dati.istruzione.it/opendata/opendata/catalogo/elements1/?area=Scuole)
*(To download the original CSV file, click on “Distribuzione per ANNOSCOLASTICO 202526” on the source page.)*

---

## 🏛️ Main Data Sheet: "scuole"

The "scuole" sheet holds the core institutional data. Below is a detailed description of the main columns included in this file:

| Column Name | Description |
| :--- | :--- |
| **ScuolaID** | *Unique numeric identifier for the school, used as the primary key.* |
| **CodiceScuola** | *Official alphanumeric Ministry of Education code for the school.* |
| **DenominazioneScuola** | *Full, official name of the school.* |
| **ComuneID** | *Foreign key linking the school to the corresponding Comune (municipality) in the "comuni" lookup sheet.* |
| **TipologiaID** | *Foreign key linking the school to the corresponding school type (Tipo di scuola) in the "tipologie" lookup sheet.* |

### Data Structure Visual

The structure of the main sheet is shown below for quick reference:

![Structure of the "scuole" sheet](assets/structure_sheet_scuole.png)

*Caption: The first columns of the "scuole" sheet, which uniquely identify each institution and link it to the lookup tables (Comuni and Tipologie).*

---
## 🔎 Lookup Sheets

The `School_Analysis.xlsx` file includes three supporting sheets used to normalize and categorize data found in the main "scuole" sheet.

### 2.1 Tipologie (School Types)

This small lookup sheet defines the classification of schools by type (e.g., Primary School, Secondary School, etc.). It helps to easily filter the main data.

| Column Name | Description |
| :--- | :--- |
| **TipologiaID** | *Unique numeric identifier for the school type (Primary Key).* |
| **Tipologia** | *Full description of the school type.* |

### 2.2 Comuni (Municipalities)

This sheet provides geographical data for the municipalities where the schools are located.

| Column Name | Description |
| :--- | :--- |
| **ComuneID** | *Unique numeric identifier for the Municipality (Primary Key), referenced by the "scuole" sheet.* |
| **Comune** | *Official name of the Italian Municipality.* |
| **ProvinciaID** | *Foreign key linking the Comune to the corresponding Province (Provincia) in the "province" lookup sheet.* |

### 2.3 Province (Provinces)

This sheet is the highest-level geographical lookup, linking municipalities to their respective provinces.

| Column Name | Description |
| :--- | :--- |
| **ProvinciaID** | *Unique numeric identifier for the Province (Primary Key), referenced by the "comuni" sheet.* |
| **Provincia** | *Full name of the Italian Province.* |
| **Sigla** | *Official two-letter abbreviation/code for the Province.* |

---
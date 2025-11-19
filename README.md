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

![Structure of the "scuole" sheet](assets/struttura_foglio_scuole.png)

*Caption: The first columns of the "scuole" sheet, which uniquely identify each institution and link it to the lookup tables (Comuni and Tipologie).*

---
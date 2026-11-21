# FarmTrack – Farming System Database (`Ariella_29031_FarmTrack`)

* **Student Name:** IRIZA NTAGANDA Ariella
* **Student ID:** 29031
* **Course:** INSY 8311 – Database Development with PL/SQL
* **Institution:** Adventist University of Central Africa (AUCA)
* **Instructor:** Eric Maniraguha
* **Domain:** Farming / Agriculture
* **Project Type:** Individual Capstone Project

## Project Overview & Problem Statement
Many farmers struggle to manage farm records, track crop growth, monitor resources, and control expenses, leading to errors, resource wastage, and financial losses. Manual record-keeping makes it difficult to monitor crop production, track harvests, and organize farm operations efficiently.

FarmTrack is a Farming System Database developed using Oracle Database and PL/SQL to improve farm management and agricultural operations. It provides a centralized system to manage farm information, crops, harvests, inventory, clients, client orders, sustainability metrics, and staff or volunteers while reducing post-harvest food waste and supporting better decision-making.

## Objectives
* **Main Objective:** To develop a centralized Farming System Database using Oracle PL/SQL to improve farm management, crop tracking, inventory control, and decision-making.
* **Specific Objectives:**
  1. Manage farm information and staff/volunteer records.
  2. Record crops and monitor harvest production.
  3. Manage farm inventory and available resources.
  4. Maintain client information and manage client orders.
  5. Monitor sustainability indicators related to farming.
  6. Track harvested crops and identify produce approaching expiry to prevent food waste.
  7. Generate useful reports to support farm management and decision-making.

## Data Source
* **Proposed Data Source:** Rwanda National Institute of Statistics (NISR) Microdata Portal (`https://www.microdatabk.statistics.gov.rw/catalog/123`)
* **Details & Verification:** Intended to provide agricultural data for Rwanda to support crop production and harvest-related records. Exact variables, record count, and educational-use licence are subject to verification, and no personally identifiable information of real people is used. Where operational data (such as client orders, staff records, or inventory transactions) is not present in the dataset, clearly identified sample records may be used for testing.

## Phase I – Business Process Documentation
* [Business Process Diagram (BPMN 2.0 PDF)](docs/business_process/business_process_diagram.pdf)
* [Business Process Explanation (PDF)](docs/business_process/business_process_explanation.pdf)

## Innovation: Smart Harvest Preservation and Waste Prevention System
* **Innovation & Tools:** Smart Harvest Preservation and Waste Prevention System built with **Oracle PL/SQL** and **Oracle APEX**.
* **How It Works:**
  1. **Harvest Recording:** Stores harvested crop quantities, harvest dates, and estimated expiry dates in `HARVESTS`.
  2. **Expiry Monitoring:** Uses PL/SQL procedures and date calculations to track the expiry status of harvested crops.
  3. **Automated Alerts:** Uses PL/SQL triggers or `DBMS_SCHEDULER` to detect produce approaching expiry.
  4. **Alert Management:** Stores generated notifications in `HARVEST_ALERTS` (an innovation support table separate from the eight main tables).
  5. **Dashboard:** Uses Oracle APEX to display harvested crops, quantities, expiry dates, and alerts so farm managers can prioritize sales and distribution and reduce post-harvest waste.

## Planned Tables and PL/SQL Features
* **Main Database Tables (8):**
  * `FARMS` – Stores farm details and information.
  * `CROPS` – Stores crop names, types, and related information.
  * `HARVESTS` – Records harvested crops, quantities, and harvest dates.
  * `INVENTORY` – Tracks available farm resources and stock.
  * `CLIENTS` – Stores client information.
  * `CLIENT_ORDER` – Records client orders and purchases.
  * `SUSTAINABILITY_METRICS` – Tracks sustainability indicators related to farming.
  * `STAFF_VOLUNTEERS` – Stores farm staff and volunteer information.
  * *(Plus `HARVEST_ALERTS` to support automated harvest expiry alerts.)*
* **Planned PL/SQL Features:**
  * **Procedures:** Register farms, add crops, record harvests, manage orders, and update inventory.
  * **Functions:** Calculate total harvest quantities, available inventory, and production statistics.
  * **Cursors:** Retrieve and process crop production, harvest, inventory, and client order records.
  * **Triggers:** Automatically detect low inventory and generate harvest expiry alerts.
  * **Packages:** Group related procedures and functions into organized modules.
  * **Exception Handling:** Handle invalid records, missing information, and duplicate entries.
  * **`DBMS_SCHEDULER`:** Schedule automatic checks for harvested crops approaching expiry.

## References (APA)
* Add your APA-formatted references from `docs/research/research_log.md` (at least 6 verified sources you have read, including research papers, a report/statistic, an existing system, a dataset, and a technical source).

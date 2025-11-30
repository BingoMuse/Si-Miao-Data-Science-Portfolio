## LegalAid Call Flow Visualization
* **Context:** Coursework (Social Impact)
* **Tools:** Microsoft Power BI, Data Modeling (DAX), ETL (Python/Pandas)
* **Key Techniques:** Hierarchical Drill-downs, Sequential Data Mapping, Call Lifecycle Analysis

### Project Objective
Designed an interactive Power BI dashboard to visualize call flow data for LegalAid, an organization providing legal services to low-income residents in Chicago. The goal was to translate raw call logs into actionable insights to improve operational efficiency, specifically by rationalizing low-volume lines and optimizing the "Main Number" routing system.

### Technical Implementation
To ensure the dashboard accurately reflected the client experience, significant data preprocessing was required before visualization:
* **Sequential Flow Mapping:** Processed the `AllCallsData` dataset to map linear journeys for every call. Transformed the data so each row represents a complete flow (Intake Number → Transfer 1 → Transfer 2 → Transfer 3), allowing for precise tracking of call depth.
* **Termination Logic:** Implemented an "Ended" category for every sequential step. This logic distinguishes between a call being successfully resolved/dropped at step *n* versus being transferred to step *n+1*, enabling precise visualization of drop-off rates at every stage.
* **Data Integrity:** Corrected initial data handling issues by removing duplicated "legs" for transfer numbers. This ensured that originating and terminating records were not double-counted, resulting in a strictly accurate count of unique connections.

### 📸 Dashboard Demo
![Drill Down Functionality Demo](./images/drill_down.gif)

### Feature Highlight: Unified Call Flow Drill-Down
To solve the complexity of analyzing scattered routing paths, I developed a unified drill-down hierarchy. This single interactive chart allows stakeholders to trace the full lifecycle of a call from intake to final termination:
1.  **Macro Level:** Aggregated call volume by Intake Lines to identify high-traffic entry points.
2.  **Flow Depth:** Visualization of the transfer network, identifying where calls are routed (e.g., Housing vs. Family Law).
3.  **Micro Level:** Outcome status (Resolved, Voicemail, Transferred) at the leaf level.

![Dashboard Overview Static](./images/dashboard_main.png)

### Key Insights & Impact
The analysis provided data-backed recommendations for LegalAid’s resource allocation:
* **Complexity Centralization:** Revealed that the "Main Number" is a bottleneck, handling nearly **50%** of all calls that require two or more connections.
* **Resource Optimization:** Identified specific specialized lines with minimal transfers, supporting a recommendation to consolidate these low-volume numbers to reduce costs.
* **Unknown Call Investigation:** Highlighted a high volume of 'Unknown' call types, prompting a targeted investigation into data entry gaps.

***
* **Note on Data Privacy:** *Due to the sensitive nature of legal client data, the raw `.pbix` file and datasets are not included in this repository. Above are static demonstrations of the dashboard's functionality and logic.*
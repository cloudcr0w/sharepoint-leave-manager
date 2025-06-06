# 📅 SharePoint Leave Manager
![Power Platform](https://img.shields.io/badge/Microsoft-Power_Platform-742774?logo=powerapps&logoColor=white)
![Status](https://img.shields.io/badge/Version-MOCK%20v1.0-blue)
![Project Type](https://img.shields.io/badge/Type-Leave%20Management%20App-lightgrey)
![Built With](https://img.shields.io/badge/Built_with-SharePoint%20%7C%20Power%20Apps%20%7C%20Power%20Automate-00adef)
![Repo status](https://img.shields.io/badge/Status--Ready_for_expansion-green)

## 🇬🇧 Project Description

A lightweight leave request system built with Microsoft 365 tools: SharePoint Online, Power Automate, and Power Apps (mock version). The solution simulates a real approval workflow and is ready for further development (Teams, BI dashboards, data migration, etc.).

---
📄 [Wersja polska](./README.md)

### 🔧 Features v1.0

- SharePoint list `LeaveRequests` with custom fields
- Power Apps form for submitting requests
- Power Apps gallery showing only requests for the logged-in user
- Power Automate approval flow (email + condition logic)
- Status auto-update + optional manager comment
- Screenshot-based documentation
- Ready for Power Platform and Teams integrations

---
## File structure
```json
📁 docs/
├─ data-import-plan.md         # Excel data migration plan
├─ flow-description.md         # Power Automate approval flow description
└─ troubleshooting.md          # Known issues and troubleshooting tips

📁 screenshots/
├─ form-submit-clean.png                 # Clean leave request form (Power Apps)
├─ form-submit-with-navi-button.png     # Form with "My requests" button
├─ my-request-view-with-navi-button.png # Filtered user gallery with navigation
└─ list-view.png                         # SharePoint list view (LeaveRequests)

📁 sharepoint/
└─ list-schema.md              # SharePoint list column definitions

📄 README.md                   # Main documentation entry point
```


### 🛣️ Roadmap

+ [x] Power Apps form (submit request)
+ [x] "My leave requests" view (user filter)
- [ ] Power BI dashboard or SharePoint view with KPIs
- [ ] Teams alert integration
- [ ] CSV export + Excel import (migration case)
- [ ] Holiday logic validation (e.g. Outlook or Azure Function)

---

## 📄 Documentation

- 📑 [Approval Flow Description](./docs/flow-description.md)
- 🛠️ [Data Import Plan (Excel migration)](./docs/data-import-plan.md)
- 🧩 [Troubleshooting and known issues](./docs/troubleshooting.md)
- 🗂️ [SharePoint List Schema](./sharepoint/list-schema.md)


---

📌 **Note**: This is a mock version due to Microsoft 365 Developer sandbox limitations. Easily transferable to a production tenant with working permissions and real data.

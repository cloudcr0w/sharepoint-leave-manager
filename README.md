# 📅 SharePoint Leave Manager
![Power Platform](https://img.shields.io/badge/Microsoft-Power_Platform-742774?logo=powerapps&logoColor=white)
![Status](https://img.shields.io/badge/Version-MOCK%20v1.0-blue)
![Project Type](https://img.shields.io/badge/Type-Leave%20Management%20App-lightgrey)
![Built With](https://img.shields.io/badge/Built_with-SharePoint%20%7C%20Power%20Apps%20%7C%20Power%20Automate-00adef)
![Repo status](https://img.shields.io/badge/Status--Ready_for_expansion-green)

## 🇵🇱 Opis projektu

System do zarządzania wnioskami urlopowymi pracowników, zbudowany w oparciu o Microsoft 365: SharePoint Online, Power Automate oraz Power Apps. Projekt demonstruje pełny przepływ — od zgłoszenia nieobecności po automatyzację zatwierdzeń. Dodatkowo zawiera plan dalszego rozwoju z użyciem Power Platform i Microsoft Teams.

📄 [English version](./README.en.md)

---

### 📋 Lista SharePoint – `LeaveRequests`

Zawiera dane wniosków urlopowych pracowników:

- `EmployeeName` – imię i nazwisko pracownika
- `StartDate` / `EndDate` – daty rozpoczęcia i zakończenia urlopu
- `LeaveType` – typ nieobecności (Vacation, Sick, Remote, Unpaid)
- `Status` – status zgłoszenia (Pending, Approved, Rejected)
- `ManagerComments` – komentarz osoby zatwierdzającej

📸 Podgląd listy:

<img src="./screenshots/list-view.png" width="650"/>


### 📝 Formularz Power Apps

Użytkownik może przesłać wniosek o urlop, wypełniając wymagane pola i wybierając typ nieobecności:

<img src="./screenshots/form-submit-clean.png" width="400"/>


### 👤 Widok „Moje wnioski” + nawigacja

Użytkownik może przeglądać tylko własne zgłoszenia urlopowe (na podstawie `EmployeeName = User().FullName`), w formie przejrzystej galerii.  
Dostępna jest intuicyjna nawigacja między formularzem a listą wniosków:

- Przycisk „Moje wnioski” prowadzi do galerii
- Przycisk „Nowy wniosek” wraca do formularza

<img src="./screenshots/form-submit-with-navi-button.png" width="400"/>
<img src="./screenshots/my-request-view-with-navi-button.png" width="400"/>


### 🔧 Funkcjonalności v1.0

- SharePoint list `LeaveRequests` z niestandardowymi polami
- Power Apps formularz zgłoszeniowy (mock)
- Power Automate Flow:
  - Trigger: `When an item is created`
  - Akcja: wysyłka maila z przyciskami `Approve`/`Reject`
  - Aktualizacja statusu + komentarz menedżera
- Dokumentacja plików + screenshoty
- Gotowość do dalszej integracji (Teams, Power BI)

---

### 📂 Struktura plików

```json
📁 docs/
├─ data-import-plan.md         # Plan importu danych z Excela (migracja)
├─ flow-description.md         # Opis przepływu zatwierdzania (Power Automate)
└─ troubleshooting.md          # Znane problemy i rozwiązania

📁 screenshots/
├─ form-submit-clean.png                 # Czysty formularz Power Apps
├─ form-submit-with-navi-button.png     # Formularz z przyciskiem „Moje wnioski”
├─ my-request-view-with-navi-button.png # Widok galerii użytkownika z przyciskiem
└─ list-view.png                         # Widok listy SharePoint (LeaveRequests)

📁 sharepoint/
└─ list-schema.md              # Definicja kolumn listy SharePoint

📄 README.md                   # Dokument główny projektu

```

---

### 🛣️ Roadmapa

+ [x] Formularz Power Apps do zgłaszania urlopów
+ [x] Widok „Moje wnioski” z filtrem użytkownika
- [ ] Dashboard z licznikami i filtrami (Power BI / SharePoint)
- [ ] Integracja z Microsoft Teams (np. powiadomienia)
- [ ] Eksport danych do CSV
- [ ] Import historycznych wniosków z pliku Excel (np. migracja z systemu legacy)
- [ ] Walidacja: dni robocze, święta (Outlook Calendar / Azure Function)

## 📄 Dokumentacja

- 📑 [Opis przepływu zatwierdzania](./docs/flow-description.md)
- 🛠️ [Plan importu danych z Excela](./docs/data-import-plan.md)
- 🧩 [Lista problemów i rozwiązań (troubleshooting)](./docs/troubleshooting.md)
- 🗂️ [Struktura listy SharePoint](./sharepoint/list-schema.md)

---

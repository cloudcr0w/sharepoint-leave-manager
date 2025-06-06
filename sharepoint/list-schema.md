# Lista SharePoint: LeaveRequests

Lista przeznaczona do zbierania i zarządzania wnioskami urlopowymi pracowników.

## 📋 Pola listy

| Nazwa kolumny     | Typ danych              | Opis                                |
|-------------------|-------------------------|--------------------------------------|
| EmployeeName      | Single line of text     | Imię i nazwisko pracownika           |
| StartDate         | Date                    | Data rozpoczęcia urlopu              |
| EndDate           | Date                    | Data zakończenia urlopu              |
| LeaveType         | Choice (select)         | Typ urlopu: Vacation, Sick, Unpaid   |
| Status            | Choice (select)         | Status: Pending, Approved, Rejected  |
| ManagerComments   | Multiple lines of text  | Komentarze od osoby zatwierdzającej  |

## 🧪 Przykładowy wpis (w formie JSON)

```json
{
  "EmployeeName": "Adam Wrona",
  "StartDate": "2025-06-10",
  "EndDate": "2025-06-14",
  "LeaveType": "Vacation",
  "Status": "Pending",
  "ManagerComments": ""
}

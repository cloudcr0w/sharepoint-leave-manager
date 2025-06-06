# 📁 Plan importu danych do SharePoint (LeaveRequests)

Cel: umożliwić zaimportowanie istniejących danych urlopowych (np. z pliku Excel lub innego systemu HR) do listy `LeaveRequests`.

---

## 🧩 Scenariusz

1. Dane historyczne dostępne jako plik Excel:
   - Kolumny: EmployeeName, StartDate, EndDate, LeaveType, Status, ManagerComments

2. Etap 1 – przygotowanie danych:
   - Zmapowanie kolumn
   - Upewnienie się, że daty są w formacie `YYYY-MM-DD`
   - Sprawdzenie poprawności pól `LeaveType` i `Status` (muszą pasować do wyborów w SharePoint)

3. Etap 2 – import:
   - Opcja A: ręczny import przez „Quick Edit” lub Excel → SharePoint Copy/Paste
   - Opcja B: Power Automate: trigger `When file is created in OneDrive` → `Add item to SharePoint list`

4. Etap 3 – walidacja:
   - Sprawdzenie liczby rekordów
   - Test zatwierdzenia dla jednego z rekordów

---

## 🔄 Status

Ten proces nie został jeszcze wdrożony, ale jest zaplanowany jako część roadmapy.

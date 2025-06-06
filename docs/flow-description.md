# Power Automate – Flow: Zatwierdzanie wniosku urlopowego

Ten przepływ automatyzuje proces zatwierdzania urlopów zgłoszonych przez pracowników.

## 📌 Trigger

- **When an item is created** in the `LeaveRequests` list

## 🔁 Akcje

1. **Get item** – pobiera szczegóły nowego wniosku
2. **Send approval email** – wysyła maila do menadżera z przyciskami:
   - Approve
   - Reject
3. **Condition** – jeśli `Outcome = Approve`
   - zaktualizuj pole `Status` na **Approved**
   - dodaj komentarz do `ManagerComments`
4. Jeśli `Outcome = Reject`
   - zaktualizuj `Status` na **Rejected**
   - dodaj komentarz

## 📧 Przykład maila

Nowy wniosek urlopowy od Adam Wrona
Termin: 10.06.2025 - 14.06.2025
Typ: Vacation

✅ [Zatwierdź] ❌ [Odrzuć]
# 🔄 Power Automate – Flow: Zatwierdzanie wniosku urlopowego

Ten przepływ automatyzuje proces zatwierdzania urlopów zgłoszonych przez pracowników w SharePoint Online.

---

## 📌 Trigger

- **When an item is created** in the `LeaveRequests` list

---

## 🔁 Akcje

1. **Get item**  
   - Pobiera szczegóły nowego wniosku (opcjonalnie, jeśli dane nie są bezpośrednio dostępne z triggera)

2. **Send approval email**  
   - Wysyła e-mail do menedżera z przyciskami:
     - ✅ Approve
     - ❌ Reject
   - Typ zgody: `Start and wait for an approval`
   - Format wiadomości zawiera dynamiczne pola (np. imię pracownika, daty urlopu, typ)

3. **Condition**  
   - Sprawdza wynik `Outcome` z maila:
     - Jeśli **Approve**:
       - Zaktualizuj pole `Status` na `Approved`
       - Dodaj komentarz w `ManagerComments` (opcjonalnie)
     - Jeśli **Reject**:
       - Zaktualizuj `Status` na `Rejected`
       - Również wpisz komentarz

---

## 📧 Przykładowa treść e-maila

```markdown
Nowy wniosek urlopowy od: Adam Wrona
Typ: Vacation
Od: 2025-06-10
Do: 2025-06-14

✅ [Zatwierdź]  ❌ [Odrzuć]
```

## 🧩 Użyte komponenty

- **Trigger**: SharePoint – `When an item is created`
- **Approval action**: `Start and wait for an approval`
- **Logic**: `Condition`
- **Update**: `Update item` – pole `Status`, `ManagerComments`

---

## 🟢 Wynik działania

- `Status` zostaje ustawiony na `Approved` lub `Rejected`
- `ManagerComments` może zawierać uzasadnienie decyzji
- Wnioskodawca widzi zaktualizowany wpis bezpośrednio w SharePoint

---

📌 Flow może być rozszerzony w przyszłości o:
- Alert w Teams
- Dodanie załącznika do zgłoszenia
- Powiadomienie e-mail do wnioskodawcy
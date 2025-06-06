# 🐞 Troubleshooting & konfiguracja SharePoint Leave Manager

---

## ✅ Konfiguracja SharePoint

- Lista `LeaveRequests` utworzona ręcznie jako custom list
- Widok "All items" skonfigurowany z polami niestandardowymi
- Uprawnienia:
  - Właściciel: Adam Wrona
  - Członkowie: użytkownicy testowi

---

## ⚠️ Napotkane problemy

- Problem: Power Automate nie widział listy `LeaveRequests`
  - Rozwiązanie: upewniłem się, że flow jest tworzony w tym samym środowisku co lista

- Problem: Flow nie aktualizował pola `Status`
  - Rozwiązanie: pole było wymagane – dodałem wartość domyślną i poprawiłem kolejność kroków

- Problem: Email approval nie trafiał do odbiorcy
  - Rozwiązanie: zmieniłem konto testowe na takie z przypisaną licencją Microsoft 365

---

## 🔧 Notatki

- Flow używa „Start and wait for an approval” – wymaga przypisanego licencjonowanego użytkownika
- SharePoint listy nie obsługują bezpośrednio walidacji dni roboczych – planowana integracja z Outlook Calendar lub JSON-em świąt

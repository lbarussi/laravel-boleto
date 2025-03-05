### Forked from [Laravel boleto](https://github.com/eduardokum/laravel-boleto)
This project was forked due to a Febraban update on February 22, 2025, which modified the "Fator Vencimento" (Expiration Factor) used in Brazilian bank slips.

Before this update, the "Fator Vencimento" was calculated as the number of days between October 7, 1997 and the billet's due date. However, as time passed, the resulting number exceeded 4 digits, which is the maximum length allowed by the financial system.

When the Fator Vencimento surpasses 9999, financial institutions automatically interpret the due date as January 1, 2000, causing issues in billet processing.

To address this, Febraban established that starting from February 22, 2025, the Fator Vencimento will be reset to 1000 and incremented daily.

Example:
2025-02-22 → 1000
2025-02-23 → 1001
2025-02-24 → 1002
And so on...

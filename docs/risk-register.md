# Risk Register

| ID  | Risk                           | Likelihood | Impact | Mitigation                                      | Owner | Status |
| --- | ------------------------------ | ---------- | ------ | ----------------------------------------------- | ----- | ------ |
| R1  | Settlement detection ambiguity | M          | H      | Status+price cross‑check; manual override table | TBD   | Open   |
| R2  | Data gaps near close           | M          | M      | 30‑min fallback; low‑confidence flag            | TBD   | Open   |
| R3  | API/schema change              | M          | M      | Retries/backoff; config endpoints               | TBD   | Open   |

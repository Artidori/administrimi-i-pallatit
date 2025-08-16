# Administrimi i Pallatit

Aplikacion një-faqësh (SPA) për menaxhimin e banorëve, faturave dhe njoftimeve të një pallati. Krejtësisht **client-side** (HTML/CSS/JS) me ruajtje lokale në **localStorage** — s’ka server apo databazë.

## ⚙️ Veçori kryesore

- **Roli Admin & Rezident**
  - Admin: shton/ndërshkon/edito banorë, krijon fatura, poston njoftime, ndryshon statusin e faturave, print/PDF (me dhe pa ngjyra), dërgon mesazh WhatsApp.
  - Rezident: **vetëm shikon** banorët, faturat e **vete** dhe njoftimet (nuk sheh butonat “Shto …”).
- **Hyrja & Sesioni**
  - Hyrje me `ID` + `Password`. Default admin: **admin / admin**.
  - Pas hyrjes hapet automatikisht seksioni **Banorët** në një tab të ri (`#/banore`).
  - “Reset Admin” rivendos `admin/admin` dhe pastron të dhënat lokale.
- **Strukturë me Tabe**
  - `Banorët`, `Faturat`, `Njoftimet` (navigim me `hash router`).
- **Faturat**
  - Numërim automatik: `FAT-YYYY-0001`.
  - Përshkrim auto sipas muajit; status **Në pritje/Paguar**.
  - WhatsApp: gjeneron mesazh të gatshëm për pagesë.
  - Print & **PDF** (ngjyra) dhe **PDF (B/W)** ku “Afati” & “Statusi” janë **me të zezë, bold**.
- **Njoftimet**
  - Tekst + imazh (ngarkohet si DataURL, ruhet në localStorage).
- **Fjalëkalime**
  - Admin/rezident mund të **ndryshojë fjalëkalimin e vet**.
  - Admin mund të **ndryshojë fjalëkalimin e banorëve**.
- **Persistencë**
  - `localStorage` (s’ka backend). Çelësat:
    - `pal_users_v4`, `pal_session_v4`, `pal_bills_v4`, `pal_notices_v4`, `pal_inv_counter_v4`.

## 🚀 Si ta nisësh

1. Klono repo-n:
   ```bash
   git clone https://github.com/Artidori/administrimi-i-pallatit.git
   cd administrimi-i-pallatit

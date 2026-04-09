# Ćwiczenia Biurowe — PWA

15 ćwiczeń kompensacyjnych dla pracownika biurowego z timerem, instrukcjami techniki i linkami do YouTube.
Działa offline po pierwszym załadowaniu.

## Szybki deploy na GitHub Pages (5 minut)

### 1. Utwórz nowe repozytorium na GitHub
- Wejdź na https://github.com/new
- Nazwa: `cwiczenia-biurowe` (lub dowolna)
- Publiczne
- **NIE** zaznaczaj "Add a README file"
- Kliknij **Create repository**

### 2. Wrzuć pliki
Masz dwie opcje:

**Opcja A — Przez przeglądarkę (najprościej):**
- Na stronie nowo utworzonego repo kliknij **"uploading an existing file"**
- Przeciągnij WSZYSTKIE 5 plików z tego folderu:
  - `index.html`
  - `manifest.json`
  - `sw.js`
  - `icon-192.png`
  - `icon-512.png`
- Kliknij **Commit changes**

**Opcja B — Przez git / Claude Code:**
```bash
cd ścieżka/do/tego/folderu
git init
git add .
git commit -m "PWA ćwiczenia biurowe"
git branch -M main
git remote add origin https://github.com/TWOJ-USERNAME/cwiczenia-biurowe.git
git push -u origin main
```

### 3. Włącz GitHub Pages
- Wejdź w **Settings** repozytorium → **Pages** (lewe menu)
- Source: **Deploy from a branch**
- Branch: **main** / **/ (root)**
- Kliknij **Save**
- Poczekaj 1-2 minuty

### 4. Gotowe!
Twoja apka jest dostępna pod adresem:
```
https://TWOJ-USERNAME.github.io/cwiczenia-biurowe/
```

### 5. Dodaj na ekran telefonu
- Otwórz powyższy URL w Chrome na Androidzie
- Kliknij **⋮** → **Dodaj do ekranu głównego**
- Apka pojawi się jako ikona na pulpicie i będzie działać offline

## Struktura plików

```
index.html      — główna aplikacja (React, samodzielna)
manifest.json   — konfiguracja PWA (nazwa, ikony, tryb standalone)
sw.js           — service worker (cache offline)
icon-192.png    — ikona 192×192 (Android)
icon-512.png    — ikona 512×512 (splash screen)
```

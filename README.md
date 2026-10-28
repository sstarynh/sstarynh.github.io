# Piłkarz – paczka PWA (aplikacja na Androida)

W paczce:
- index.html – cała gra (jeden plik)
- manifest.json – nazwa, ikony, tryb pełnoekranowy
- sw.js – service worker (działanie offline)
- icon-192.png, icon-512.png, icon-maskable-512.png – ikony

## 1. Wrzucenie na hosting (potrzebny HTTPS)

### GitHub Pages (darmowe)
1. Załóż konto na github.com i utwórz nowe, publiczne repozytorium (np. `pilkarz`).
2. „Add file” → „Upload files” i przeciągnij wszystkie pliki z tej paczki (rozpakowane, bez folderu nadrzędnego). Zatwierdź („Commit changes”).
3. Settings → Pages → „Deploy from a branch” → branch `main`, folder `/ (root)` → Save.
4. Po 1–2 minutach gra jest pod adresem `https://TWOJ-LOGIN.github.io/pilkarz/`.

### Netlify Drop (jeszcze prościej)
1. Wejdź na app.netlify.com/drop.
2. Przeciągnij rozpakowany folder z plikami. Dostajesz adres HTTPS od razu.

## 2. Instalacja na Androidzie
1. Otwórz adres gry w Chrome na telefonie.
2. Menu (trzy kropki) → „Zainstaluj aplikację” lub „Dodaj do ekranu głównego”.
3. Ikona pojawi się na ekranie głównym i gra otworzy się jak zwykła aplikacja (pełny ekran, działa też offline po pierwszym otwarciu).
4. Wskazówka: do meczów obróć telefon poziomo.

## 3. Aktualizacja gry
1. Podmień index.html w repozytorium.
2. W sw.js zmień `pilkarz-v1` na `pilkarz-v2` (potem v3 itd.), inaczej telefony mogą trzymać starą wersję z pamięci podręcznej.

## 4. Plik APK (opcjonalnie)
1. Wejdź na pwabuilder.com i wklej adres opublikowanej gry.
2. Wybierz „Package for stores” → Android → pobierz pakiet.
3. APK instalujesz na telefonie po zezwoleniu na instalację z nieznanych źródeł. Do Google Play potrzebny jest plik AAB i konto deweloperskie.

## Uwagi
- Zapis kariery jest w pamięci przeglądarki na danym telefonie (nie przenosi się między urządzeniami).
- W grze użyte są prawdziwe nazwy klubów i piłkarzy. Do prywatnych testów to bez problemu, przed publikacją w sklepie zamień je na wymyślone.

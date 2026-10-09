# Demon Biznesu Polska

Gra handlowa w jednym pliku `index.html` (bez zależności). Kupuj tanio, sprzedawaj drożej, jeźdź po Polsce, omijaj policję.

- Budowa: `./build.sh` składa `index.html` z `part1.html` (styl), `part2.js` (dane i logika), `audio.js` (dźwięki jako base64), `engine.js` (silnik dźwięku i muzyki, głośność) i `part3.js` (grafika i interfejs).
- Dźwięki: pliki źródłowe w `audio_src/`; `python3 tools/build_audio.py` konwertuje je do `audio.js` (wymaga ffmpeg).
- Towary: 12, w tym kontrabanda z przemytem broni (najwyższy zysk i ryzyko).
- Test: `NODE_PATH=<ścieżka do playwright> node tests/smoke.js` (interfejs + balans botem). Balans ręcznie: `node tests/balance.js 30`.
- APK: `python3 tools/mkapk.py android/template.apk index.html DemonBiznesu.apk <katalog_kluczy>`.

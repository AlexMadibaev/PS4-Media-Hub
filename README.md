# PS4 Media Hub

Experimental Media Station X-inspired **web prototype**. This repository does not yet contain a native PS4 application or installable PKG.

## Implemented
- TV-style responsive portal library
- Add, edit, delete and open HTTPS portals
- Local storage, JSON import/export, input validation
- Keyboard navigation and experimental Gamepad API polling (Cross/ Circle/ D-pad mapping)

## Run locally
```bash
python -m http.server 8000 --directory web
```
Open http://localhost:8000 in a desktop browser. Connect a gamepad and press a button to activate the Gamepad API. Browser support varies.

## Limitations
- Portal navigation uses the browser, **not** an embedded PS4 WebView.
- No native PS4 build, SDK integration, PKG, streaming decoder or HLS engine.
- MSX/Lampa compatibility on actual PS4 hardware is **unverified**.
- PS4 browser may not support the Gamepad API, localStorage or portal JavaScript features.

## Roadmap
1. Confirm a redistributable PS4 homebrew SDK and reproducible hello-world PKG pipeline.
2. Test controller and browser capabilities on real GoldHEN hardware.
3. Investigate embedded portal runtime feasibility; otherwise explicitly scope to native catalog/stream playback.
4. Implement video playback only for supported codecs and lawful media sources.

CI currently validates web assets only. A passing check **does not** indicate a PS4 build.

QuizBattleWar Admin Panel — Hindi Setup

FILES
- admin.html: standalone admin panel file
- admin-site/index.html: same panel as index.html for GitHub Pages repository root

BEFORE USE
1. Upload admin-site/index.html to the root of a separate GitHub repository (e.g. Adminf) and enable GitHub Pages. Or host admin.html on another static host.
2. Firebase Authentication > Sign-in method: enable Google.
3. Firebase Authentication > Settings > Authorized domains: add the exact domain where this panel is hosted.
4. Realtime Database rules must allow only the owner UID to write appSettings, while the game must be able to read the settings it needs. Never make all database writes public.
5. Admin UID configured in this file: L0YvKVpAcKgiABKed93JgOa9qWj2
6. Gemini: get an API key from Google AI Studio and paste it in the panel when needed. Do not send the key to anyone. Browser-side API keys can be exposed; a server-side proxy is safer.
7. MUSIC UPLOAD IMPORTANT: Firebase Storage may require the Blaze billing plan for a Storage bucket. If the project is on Spark and Storage says upgrade/402/403, this upload will not work without enabling billing. Do not add billing details unless an adult/account owner approves and understands possible charges. The panel also supports publishing a direct HTTPS audio URL hosted elsewhere. The URL must be a direct audio file and allow browser playback.
8. This panel publishes questions/music/tournaments/offers to Realtime Database path appSettings. Your game must read appSettings and understand the same field names.

This is the admin panel source. It has not been tested against your live Firebase rules/project; after you configure Firebase, test login, publish, question generation, and music upload.

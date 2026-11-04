# Changelog

Notes de version de Mumo. Format : `## <version> — <date>`, `### <langue>` (en, fr, zh-Hans, zh-Hant),
`#### <catégorie>` (new, improved, fixed), puis une puce par ligne. La publication (`make release`) exige,
pour la version publiée, les quatre langues avec au moins une puce. Détails :
docs/superpowers/specs/2026-09-17-release-notes-and-update-awareness-design.md

## 0.3.0 — 2026-11-04
### en
#### new
- Murmure is now **Mumo** — same app, same settings, new name. Your dictionary, history and models are untouched.
- Chinese mode: a dedicated engine (Qwen3-ASR) for Mandarin, Cantonese and mixed Chinese-English, with live preview — enabled by default when your Mac is in Chinese. Other languages keep Whisper.
#### improved
- On a full-screen space (video, presentation…), the idle pill and island stay tucked away; only your dictation appears.
### fr
#### new
- Murmure devient **Mumo** — même app, mêmes réglages, nouveau nom. Dictionnaire, historique et modèles sont conservés.
- Mode chinois : un moteur dédié (Qwen3-ASR) pour le mandarin, le cantonais et le mélange chinois-anglais, avec aperçu en direct — activé d'office si votre Mac est en chinois. Les autres langues gardent Whisper.
#### improved
- Sur un espace plein écran (vidéo, présentation…), la pastille et l'île restent rangées au repos ; seule la dictée s'affiche.
### zh-Hans
#### new
- Murmure 更名为 **Mumo**：同一款应用、同样的设置，只是换了名字。词典、历史记录和模型均保持不变。
- 中文模式：专用引擎（Qwen3-ASR）支持普通话、粤语及中英混说，并提供实时预览；Mac 为中文时默认开启。其他语言仍使用 Whisper。
#### improved
- 在全屏空间（视频、演示等）中，闲置的胶囊和灵动岛保持隐藏，只显示听写内容。
### zh-Hant
#### new
- Murmure 更名為 **Mumo**：同一款應用、同樣的設定，只是換了名字。字典、歷史記錄和模型均保持不變。
- 中文模式：專用引擎（Qwen3-ASR）支援國語、粵語及中英混說，並提供即時預覽；Mac 為中文時預設開啟。其他語言仍使用 Whisper。
#### improved
- 在全螢幕空間（影片、簡報等）中，閒置的膠囊和動態島保持隱藏，只顯示聽寫內容。

## 0.2.0 — 2026-09-17
### en
#### new
- The bottom pill unfolds into the style menu on hover; the menu opens with intent (a short pause), never on a quick mouse pass.
- Release notes are shown after every update, and available from About.
- Updates are detected in the background and signaled discreetly (menu bar dot, menu item, short notice).
#### fixed
- No more ghost menu when switching desktops quickly.
- The style menu no longer went dead on some desktops.
### fr
#### new
- La pastille se déploie elle-même en menu au survol ; le menu s'ouvre avec intention (courte pause), jamais au simple passage de la souris.
- Les nouveautés s'affichent après chaque mise à jour, et restent consultables depuis « À propos ».
- Les mises à jour sont détectées en arrière-plan et signalées discrètement (point sur l'icône, item de menu, courte notice).
#### fixed
- Plus d'image fantôme du menu lors des changements de bureau rapides.
- Le menu de styles ne restait plus inerte sur certains bureaux.
### zh-Hans
#### new
- 底部胶囊在悬停时自行展开为样式菜单；菜单需要短暂停留才会打开，鼠标快速掠过不会触发。
- 每次更新后显示新功能说明，并可随时在“关于”中查看。
- 在后台检测更新并以不打扰的方式提示（菜单栏小圆点、菜单项、简短提示）。
#### fixed
- 快速切换桌面时不再出现菜单残影。
- 样式菜单在某些桌面上不再失效。
### zh-Hant
#### new
- 底部膠囊在懸停時自行展開為樣式選單；選單需要短暫停留才會開啟，滑鼠快速掠過不會觸發。
- 每次更新後顯示新功能說明，並可隨時在「關於」中查看。
- 在背景偵測更新並以不打擾的方式提示（選單列小圓點、選單項目、簡短提示）。
#### fixed
- 快速切換桌面時不再出現選單殘影。
- 樣式選單在某些桌面上不再失效。

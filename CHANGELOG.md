# Changelog

Notes de version de Mumo. Format : `## <version> — <date>`, `### <langue>` (en, fr, zh-Hans, zh-Hant),
`#### <catégorie>` (new, improved, fixed), puis une puce par ligne. La publication (`make release`) exige,
pour la version publiée, les quatre langues avec au moins une puce. Détails :
docs/superpowers/specs/2026-09-17-release-notes-and-update-awareness-design.md

## 0.4.0 — 2026-11-08
### en
#### new
- Translation is now a feature of its own, on Apple's engine (macOS 26): turn on “Translate what I dictate” from the island menu, the menu bar or Settings › Translation, pick the language, and dictate. The island and the capsule show the target while it's on, a “Translate once” shortcut handles one-off dictations, and each app can have its own language.
- Translations and restyles of selected text now land in History too, as their own kind: a “Selection” tag, a filter (All, Dictations, Selection), the original one click away, and nothing counted in your dictation stats.
- Setup now ends with your first real dictation: press your shortcut, speak, and see the text: with the tips that matter (hold or tap, the preview is just a preview, ⌘V, Esc, History).
- Translation gets its own setup step: turn it on, pick the language, see what it does. And setup now ends with two dictations: your first one, then the same gesture translated into the language you pick, your first sentence translated live while you wait, the original kept under the result.
#### improved
- Translate selection and Restyle selection now share one sheet that opens right in the island or the capsule, with Translate and Restyle tabs: the text you selected (editable), the language or style, and the result shown in place, copied for you if you want. ✕, Esc or a click anywhere else closes it. Translation uses Apple's engine: every language macOS offers, nothing to download on a Mac with Apple Intelligence, and the language you pick there applies to that translation only.
- The island menu is down to five rows: Style (the styles live one level down, yours after a divider), Translate, Re-run last dictation, Selected text… and Settings. “Raw” is now called “No style”.
- The island and the capsule now show the active style's symbol next to the translation badge, at rest and while you dictate, so you never forget a style is on.
- Settings › Formatting no longer shows a “No style” card: turning cleanup off is the way to dictate without a style, and “No style” stays in the island menu as the quick switch.
- Style cards stay active while cleanup is off: picking a style turns cleanup on, and an API-key style never asks you to download the local model.
- API keys are managed in one place, Settings › Formatting: add, rename in place, delete, with a badge saying which styles use each key and a named warning before deleting a key a style depends on.
- Formatting now shows built-in styles and your own styles as two groups; Storage rows line up (sizes in a column, same-size buttons, “In use” as a badge).
- History text can be selected with the mouse again, with a clean right-click menu (Copy, the other version).
- On an 8 GB Mac, text cleanup is now off by default during setup (you can turn it on anytime); the Styles step is skipped while cleanup is off, but you still get a preview of what cleanup and styles do.
- During setup, models download only after you tap Continue; changing your mind cancels and removes what was downloaded.
- The red badge now also sits on the “Update to…” menu line, so you can see where the notification comes from.
- Translation's default language is no longer always English: it's your Mac's second language when it has one, never the language Mumo is displayed in.
- Turning on cleanup without the local model now also offers “Use an API key instead”: format through your own key, no 4 GB download. The Formatting tab says where formatting runs (on your Mac, or through which provider).
- Dictation settings: the Chinese mode switch now sits at the top of Transcription, and the Whisper models fold away while it's on, during setup too.
- Dictionary: one field and an “Add” button; the replacement is tucked behind “Make it a snippet”. The setup demo now says what it shows (a word, a snippet) and runs slower.
- A simpler window: Home, History, Dictionary and Settings in the sidebar; General, Dictation, Formatting, Appearance and Storage are now tabs inside Settings. The menu bar menu follows: Settings…, Dictionary…, History….
#### fixed
- A dictation with no recognized speech now says so, instead of doing nothing.
- Time saved no longer shows 0 when your dictations include pauses: speech time now counts only the time you actually spend talking.
- Custom styles on an API key work again: Claude models refused one of our parameters and the fallback pasted the raw text silently. Mumo now adapts its request to each model, tells you when a cloud engine fails, and frames custom prompts so the model rewrites your dictation instead of answering it.
- A style can no longer change or drop a number: if a date, a count or a time differs between what you said and the result, Mumo pastes your words as dictated.
- Chinese mode: a dictation no longer comes back empty on the first try when the last slice of audio decodes to nothing; Mumo keeps what it already heard and, if in doubt, re-reads the whole recording before saying “no words recognized”.
### fr
#### new
- La traduction devient une fonction à part entière, sur le moteur d'Apple (macOS 26) : activez « Traduire ce que je dicte » depuis le menu de l'île, la barre des menus ou Réglages › Traduction, choisissez la langue, dictez. L'île et la capsule affichent la langue tant que c'est actif, un raccourci « traduire une fois » sert aux dictées ponctuelles, et chaque app peut avoir sa propre langue.
- Les traductions et remises en forme d'un texte sélectionné entrent aussi dans l'Historique, à part : une étiquette « Sélection », un filtre (Tout, Dictées, Sélection), l'original à un clic, et rien de compté dans vos statistiques de dictée.
- La configuration se termine désormais par votre première vraie dictée : appuyez sur votre raccourci, parlez, et voyez le texte : avec les conseils qui comptent (maintenir ou taper, l'aperçu n'est qu'un aperçu, ⌘V, Échap, Historique).
- La traduction a son étape dans la configuration : l'allumer, choisir la langue, voir ce qu'elle fait. Et la configuration se termine désormais par deux dictées : la première, puis le même geste traduit dans la langue de votre choix, votre première phrase traduite en direct en attendant, l'original gardé sous le résultat.
#### improved
- Traduire la sélection et Restyler la sélection tiennent désormais dans une seule fiche qui s'ouvre dans l'île ou la capsule, avec les onglets Traduire et Restyler : le texte sélectionné (modifiable), la langue ou le style, et le résultat affiché sur place, copié pour vous si vous le souhaitez. ✕, Échap ou un clic n'importe où ailleurs la ferme. La traduction passe par le moteur d'Apple : toutes les langues de macOS, rien à télécharger sur un Mac avec Apple Intelligence, et la langue choisie là ne vaut que pour cette traduction.
- Le menu de l'île tient en cinq lignes : Style (les styles sont un niveau plus bas, les vôtres après un séparateur), Traduire, Rejouer la dernière dictée, Texte sélectionné… et Réglages. « Brut » s'appelle désormais « Sans style ».
- L'île et la capsule affichent le symbole du style actif à côté du badge de traduction, au repos et pendant la dictée : on n'oublie plus qu'un style est activé.
- Réglages › Mise en forme n'affiche plus de carte « Sans style » : couper le nettoyage est la façon de dicter sans style, et « Sans style » reste dans le menu de l'île comme coupure rapide.
- Les cartes de style restent actives quand le nettoyage est coupé : choisir un style l'allume, et un style sur clé API ne demande jamais de télécharger le modèle local.
- Les clés API se gèrent à un seul endroit, Réglages › Mise en forme : ajout, renommage sur place, suppression, avec une pastille qui dit quels styles utilisent chaque clé et un avertissement nominatif avant de supprimer une clé dont un style dépend.
- Mise en forme sépare désormais les styles fournis de vos styles ; les lignes de Stockage sont alignées (tailles en colonne, boutons de même taille, « Utilisé » en pastille).
- Le texte de l'historique se sélectionne de nouveau à la souris, avec un clic droit propre (Copier, l'autre version).
- Sur un Mac de 8 Go, le nettoyage du texte est désormais coupé par défaut à la configuration (activable à tout moment) ; l'étape Styles est passée tant qu'il est coupé, mais vous voyez quand même ce que font le nettoyage et les styles.
- Pendant la configuration, les modèles ne se téléchargent qu'après « Continuer » ; changer d'avis annule et supprime ce qui avait été téléchargé.
- Le badge rouge figure aussi sur la ligne « Mettre à jour vers… » du menu : on voit d'où vient la notification.
- La langue de traduction par défaut n'est plus toujours l'anglais : c'est la deuxième langue de votre Mac quand il en a une, jamais la langue d'affichage de Mumo.
- Activer le nettoyage sans le modèle local propose aussi « Utiliser une clé API à la place » : mise en forme avec votre propre clé, sans les 4 Go. L'onglet Mise en forme dit où tourne la mise en forme (sur votre Mac, ou via quel fournisseur).
- Réglages Dictée : l'interrupteur du mode chinois est en tête de Transcription, et les modèles Whisper se replient tant qu'il est actif, pendant la configuration aussi.
- Dictionnaire : un seul champ et un bouton « Ajouter » ; le remplacement est rangé derrière « En faire un snippet ». La démo de la configuration dit désormais ce qu'elle montre (un mot, un snippet) et va moins vite.
- Une fenêtre plus simple : Accueil, Historique, Dictionnaire et Réglages dans la barre latérale ; Général, Dictée, Mise en forme, Apparence et Stockage sont désormais des onglets dans Réglages. Le menu de la barre des menus suit : Réglages…, Dictionnaire…, Historique….
#### fixed
- Une dictée sans parole reconnue le dit maintenant, au lieu de ne rien faire.
- Le temps gagné ne tombe plus à 0 quand vos dictées contiennent des pauses : le temps de parole ne compte plus que le temps réellement passé à parler.
- Les styles perso sur clé API fonctionnent de nouveau : les modèles Claude refusaient un de nos paramètres et le repli collait le texte brut sans rien dire. Mumo adapte désormais sa requête à chaque modèle, prévient quand un moteur cloud échoue, et cadre les prompts perso pour que le modèle réécrive la dictée au lieu d'y répondre.
- Un style ne peut plus changer ni perdre un nombre : si une date, un compte ou une heure diffère entre ce que vous avez dit et le résultat, Mumo colle vos mots tels que dictés.
- Mode chinois : une dictée ne revient plus vide au premier essai quand la dernière tranche d'audio ne donne rien ; Mumo garde ce qu'il a déjà entendu et, en cas de doute, relit tout l'enregistrement avant de dire « aucun mot reconnu ».
### zh-Hans
#### new
- 翻译成为独立功能，基于 Apple 引擎（macOS 26）：在灵动岛菜单、菜单栏或“设置 › 翻译”中开启“翻译我的听写”，选择语言，然后听写。开启期间灵动岛和胶囊会显示目标语言，“翻译一次”快捷键用于单次听写，每个应用也可设置自己的语言。
- 对所选文字的翻译和套用样式现在也进入历史记录，单独归类：“所选内容”标签、筛选器（全部、听写、所选内容）、一键查看原文，且不计入听写统计。
- 初始设置现在以你的第一次真实听写结束：按下快捷键、说话、看到文字，并附上要点提示（长按或点按、预览只是预览、⌘V、Esc、历史记录）。
- 翻译在初始设置中有了自己的步骤：开启、选择语言、了解它能做什么。初始设置现在以两次听写结束：先是第一次听写，然后用同样的手势听写一句、翻译成你选择的语言；等待时会实时翻译你的第一句话，原文保留在结果下方。
#### improved
- “翻译所选内容”和“套用样式”现在合并为一个面板，直接在灵动岛或胶囊中打开，含“翻译”和“套用样式”两个标签：所选文字（可编辑）、语言或风格，以及就地显示的结果，需要时自动拷贝。✕、Esc 或点击其他任意处即可关闭。翻译使用 Apple 引擎：支持 macOS 提供的所有语言，配备 Apple Intelligence 的 Mac 无需下载，面板中选择的语言仅对本次翻译有效。
- 灵动岛菜单精简为五行：风格（各风格收在下一级，自定义风格在分隔线之后）、翻译、重新运行上次听写、所选文字…和设置。“原文”改名为“无风格”。
- 灵动岛和胶囊现在会在翻译标记旁显示当前风格的符号，待机和听写时都可见，不会再忘记已开启某个风格。
- “设置 › 格式”不再显示“无风格”卡片：关闭清理即可按原样听写，“无风格”仍保留在灵动岛菜单中作为快捷开关。
- 清理关闭时风格卡片仍可点击：选择一个风格即开启清理，使用 API 密钥的风格不会要求下载本地模型。
- API 密钥集中在“设置 › 格式”中管理：添加、就地重命名、删除，并显示每个密钥被哪些风格使用；删除有风格依赖的密钥前会点名提醒。
- “格式”现在将内置风格与你的风格分为两组；“存储”各行对齐（大小单独成列、按钮同样大小、“使用中”显示为标记）。
- 历史记录中的文字可以再次用鼠标选取，右键菜单干净利落（拷贝、另一版本）。
- 8 GB 内存的 Mac 上，初始设置时文本清理默认关闭（可随时开启）；关闭期间跳过“风格”步骤，但仍会预览清理和风格的效果。
- 初始设置中，模型仅在点击“继续”后才开始下载；改变主意会取消并删除已下载的内容。
- 红色角标现在也显示在菜单的“更新到…”一行，一眼看出通知来源。
- 翻译的默认语言不再总是英语：如果你的 Mac 设置了第二语言，就用它，且绝不会是 Mumo 的显示语言。
- 在没有本地模型时开启清理，现在还可选择“改用 API 密钥”：用你自己的密钥进行格式化，无需下载 4 GB。“格式”标签页会说明格式化在哪里进行（你的 Mac 上，或通过哪个服务商）。
- 听写设置：中文模式开关移到“转录”顶部，开启期间 Whisper 模型会折叠起来，初始设置中也一样。
- 词典：只有一个输入框和“添加”按钮；替换文字收在“设为片段”之下。初始设置的演示现在会说明展示的是什么（一个词、一个片段），速度也放慢了。
- 窗口更简洁：侧边栏只有主页、历史记录、词典和设置；通用、听写、格式、外观和存储现在是设置内的标签页。菜单栏菜单同步精简为：设置…、词典…、历史记录…。
#### fixed
- 未识别到语音的听写现在会给出提示，而不是毫无反应。
- 听写中有停顿时，“节省时间”不再显示 0：语音时长现在只计算真正说话的时间。
- 使用 API 密钥的自定义风格恢复正常：Claude 模型拒绝了我们的某个参数，回退时静默粘贴了原文。Mumo 现在会根据模型调整请求，在云端引擎失败时提示，并为自定义提示词加上框架，让模型改写听写内容而不是回答它。
- 风格不再会改动或丢失数字：若日期、数量或时间与你所说的不一致，Mumo 会按原样粘贴你的话。
- 中文模式：当最后一段音频解码为空时，听写不再在第一次就返回空白；Mumo 会保留已听到的内容，必要时重新识别整段录音，再判断“未识别到语音”。
### zh-Hant
#### new
- 翻譯成為獨立功能，基於 Apple 引擎（macOS 26）：在動態島選單、選單列或「設定 › 翻譯」中開啟「翻譯我的聽寫」，選擇語言，然後聽寫。開啟期間動態島和膠囊會顯示目標語言，「翻譯一次」快速鍵用於單次聽寫，每個 App 也可設定自己的語言。
- 對所選文字的翻譯和套用樣式現在也進入歷史記錄，單獨歸類：「所選內容」標籤、篩選器（全部、聽寫、所選內容）、一鍵查看原文，且不計入聽寫統計。
- 初始設定現在以你的第一次真實聽寫結束：按下快速鍵、說話、看到文字，並附上要點提示（長按或點按、預覽只是預覽、⌘V、Esc、歷史記錄）。
- 翻譯在初始設定中有了自己的步驟：開啟、選擇語言、了解它能做什麼。初始設定現在以兩次聽寫結束：先是第一次聽寫，然後用同樣的手勢聽寫一句、翻譯成你選擇的語言；等待時會即時翻譯你的第一句話，原文保留在結果下方。
#### improved
- 「翻譯所選內容」和「套用樣式」現在合併為一個面板，直接在動態島或膠囊中打開，含「翻譯」和「套用樣式」兩個標籤：所選文字（可編輯）、語言或樣式，以及就地顯示的結果，需要時自動拷貝。✕、Esc 或點按其他任意處即可關閉。翻譯使用 Apple 引擎：支援 macOS 提供的所有語言，配備 Apple Intelligence 的 Mac 無需下載，面板中選擇的語言僅對本次翻譯有效。
- 動態島選單精簡為五行：風格（各風格收在下一級，自訂風格在分隔線之後）、翻譯、重新執行上次聽寫、所選文字…和設定。「原文」改名為「無風格」。
- 動態島和膠囊現在會在翻譯標記旁顯示目前風格的符號，待機和聽寫時都可見，不會再忘記已開啟某個風格。
- 「設定 › 格式」不再顯示「無風格」卡片：關閉清理即可按原樣聽寫，「無風格」仍保留在動態島選單中作為快速開關。
- 清理關閉時樣式卡片仍可點按：選擇一個樣式即開啟清理，使用 API 金鑰的樣式不會要求下載本機模型。
- API 金鑰集中在「設定 › 格式」中管理：加入、就地重新命名、刪除，並顯示每個金鑰被哪些樣式使用；刪除有樣式依賴的金鑰前會點名提醒。
- 「格式」現在將內建樣式與你的樣式分為兩組；「儲存空間」各列對齊（大小獨立成欄、按鈕大小一致、「使用中」顯示為標記）。
- 歷史記錄中的文字可以再次用滑鼠選取，右鍵選單乾淨俐落（拷貝、另一版本）。
- 8 GB 記憶體的 Mac 上，初始設定時文字清理預設關閉（可隨時開啟）；關閉期間略過「風格」步驟，但仍會預覽清理和風格的效果。
- 初始設定中，模型僅在點按「繼續」後才開始下載；改變主意會取消並刪除已下載的內容。
- 紅色標記現在也顯示在選單的「更新至…」一行，一眼看出通知來源。
- 翻譯的預設語言不再總是英文：如果你的 Mac 設定了第二語言，就用它，且絕不會是 Mumo 的顯示語言。
- 在沒有本機模型時開啟清理，現在還可選擇「改用 API 金鑰」：用你自己的金鑰進行格式化，無需下載 4 GB。「格式」標籤頁會說明格式化在哪裡進行（你的 Mac 上，或透過哪個服務商）。
- 聽寫設定：中文模式開關移到「轉錄」頂部，開啟期間 Whisper 模型會摺疊起來，初始設定中也一樣。
- 字典：只有一個輸入框和「新增」按鈕；替換文字收在「設為片段」之下。初始設定的示範現在會說明展示的是什麼（一個詞、一個片段），速度也放慢了。
- 視窗更簡潔：側邊欄只有主頁、歷史記錄、字典和設定；通用、聽寫、格式、外觀和儲存現在是設定內的標籤頁。選單列選單同步精簡為：設定…、詞典…、歷史記錄…。
#### fixed
- 未辨識到語音的聽寫現在會給出提示，而不是毫無反應。
- 聽寫中有停頓時，「節省時間」不再顯示 0：語音時長現在只計算真正說話的時間。
- 使用 API 金鑰的自訂樣式恢復正常：Claude 模型拒絕了我們的某個參數，回退時靜默貼上了原文。Mumo 現在會根據模型調整請求，在雲端引擎失敗時提示，並為自訂提示詞加上框架，讓模型改寫聽寫內容而不是回答它。
- 樣式不再會改動或遺漏數字：若日期、數量或時間與你所說的不一致，Mumo 會按原樣貼上你的話。
- 中文模式：當最後一段音訊解碼為空時，聽寫不再在第一次就傳回空白；Mumo 會保留已聽到的內容，必要時重新辨識整段錄音，再判斷「未辨識到語音」。

## 0.3.0 — 2026-11-04
### en
#### new
- Murmure is now **Mumo**: same app, same settings, new name. Your dictionary, history and models are untouched.
- Chinese mode: a dedicated engine (Qwen3-ASR) for Mandarin, Cantonese and mixed Chinese-English, with live preview: enabled by default when your Mac is in Chinese. Other languages keep Whisper.
#### improved
- On a full-screen space (video, presentation…), the idle pill and island stay tucked away; only your dictation appears.
### fr
#### new
- Murmure devient **Mumo** : même app, mêmes réglages, nouveau nom. Dictionnaire, historique et modèles sont conservés.
- Mode chinois : un moteur dédié (Qwen3-ASR) pour le mandarin, le cantonais et le mélange chinois-anglais, avec aperçu en direct : activé d'office si votre Mac est en chinois. Les autres langues gardent Whisper.
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

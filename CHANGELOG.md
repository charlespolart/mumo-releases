# Changelog

Notes de version de Mumo. Format : `## <version> · <date>`, `### <langue>` (en, fr, zh-Hans, zh-Hant),
`#### <catégorie>` (new, improved, fixed), puis une puce par ligne. La publication (`make release`) exige,
pour la version publiée, les quatre langues avec au moins une puce. Détails :
docs/superpowers/specs/2026-09-17-release-notes-and-update-awareness-design.md

## 0.5.0 · 2026-11-13
### en
#### new
- Live subtitles: Mumo shows what is said in the sound your Mac plays, a film, a video, a call, even with the volume at zero. Listen to the whole Mac or one app, read it in the spoken language or translated, detach it into a panel you can place anywhere, and keep the transcript in History if you want a record. Everything stays on your Mac. Requires macOS 14.2; translation requires macOS 26.
#### improved
- Setup: text cleanup is now off when setup ends, so your first dictations are written right away. Setup still shows what it does; turn it on in Settings › Formatting when you want it.
- Setup: with Chinese mode on, you now choose Simplified or Traditional right there. It is preselected from your interface language.
- Settings: the Chinese engine now shows its size, under Chinese mode and in Storage, where it can be deleted once Chinese mode is off.
#### fixed
- Chinese mode: a dictation could stop writing partway, after about 50 seconds when it had pauses or after a few minutes without, and lose everything said afterwards, without any error. The end of a sentence before a long pause, or a first word followed by a long silence, could also disappear. Dictation no longer stops writing.
- Chinese mode: when you ended a dictation while its last words were still being transcribed, the end of the text could be cut off, or a short dictation could be replaced by a stray “Language French”. The last words are now always transcribed in full.
- Chinese mode: with Simplified selected, the live preview of a Cantonese dictation showed Traditional characters before the final text. The preview now follows the chosen script.
### fr
#### new
- Sous-titres en direct : Mumo affiche ce qui se dit dans le son que votre Mac émet, un film, une vidéo, un appel, même le volume à zéro. Écoutez tout le Mac ou une seule app, lisez dans la langue parlée ou traduit, détachez le texte dans un panneau à placer où vous voulez, et gardez la transcription dans l'Historique pour en faire un compte rendu. Tout reste sur votre Mac. Nécessite macOS 14.2 ; la traduction nécessite macOS 26.
#### improved
- Configuration : le nettoyage du texte est désormais coupé à la fin de la configuration, pour que vos premières dictées s'écrivent tout de suite. La configuration montre toujours ce qu'il fait ; activez-le dans Réglages › Mise en forme quand vous le voulez.
- Configuration : avec le mode chinois, vous choisissez maintenant l'écriture simplifiée ou traditionnelle sur place. Elle est présélectionnée d'après la langue de l'interface.
- Réglages : le moteur chinois affiche désormais sa taille, sous le mode chinois et dans Stockage, où il peut être supprimé une fois le mode chinois coupé.
#### fixed
- Mode chinois : une dictée pouvait cesser d'écrire en cours de route, après environ 50 secondes si elle comportait des pauses, quelques minutes sinon, et perdre tout ce qui était dit ensuite, sans erreur. La fin d'une phrase avant une longue pause, ou un premier mot suivi d'un long silence, pouvait aussi disparaître. La dictée ne cesse plus d'écrire.
- Mode chinois : quand vous terminiez une dictée pendant que ses derniers mots étaient encore en cours de transcription, la fin du texte pouvait être coupée, ou une courte dictée remplacée par un « Language French » parasite. Les derniers mots sont désormais toujours transcrits en entier.
- Mode chinois : avec « Simplifié » choisi, l'aperçu en direct d'une dictée en cantonais montrait des caractères traditionnels avant le texte final. L'aperçu suit désormais l'écriture choisie.
### zh-Hans
#### new
- 实时字幕：Mumo 显示 Mac 播放的声音中所说的内容，电影、视频、通话都可以，即使音量为零也行。可收听整台 Mac 或单个应用，按原语言阅读或翻译后阅读，可将文字分离到面板并放在任意位置，也可将转录内容保留在历史记录中作为记录。所有内容都留在你的 Mac 上。需要 macOS 14.2；翻译需要 macOS 26。
#### improved
- 初始设置：文本清理现在在设置结束时默认关闭，让你的第一次听写立即写出。设置过程仍会演示它的作用；需要时可在“设置 › 格式”中开启。
- 初始设置：开启中文模式后，现在可以直接选择简体或繁体，并会根据界面语言预先选好。
- 设置：中文引擎现在会显示其大小，位于中文模式下方和“存储”中；关闭中文模式后可在“存储”中删除。
#### fixed
- 中文模式：听写可能中途停止写入（有停顿时约 50 秒后，没有停顿时几分钟后），之后说的内容全部丢失，而且没有任何错误提示。长时间停顿前的句尾，或开头一个词后跟着长时间静音，也可能消失。现在听写不会再中途停止写入。
- 中文模式：如果在最后几个词仍在转写时结束听写，文本结尾可能被截断，或者较短的听写会被一段多余的“Language French”取代。现在最后几个词总会完整转写。
- 中文模式：选择“简体”时，粤语听写的实时预览会先显示繁体字，最终文本才是简体。现在预览会按所选字体显示。
### zh-Hant
#### new
- 即時字幕：Mumo 顯示 Mac 播放的聲音中所說的內容，電影、影片、通話都可以，即使音量為零也行。可收聽整台 Mac 或單一 App，按原語言閱讀或翻譯後閱讀，可將文字分離到面板並放在任意位置，也可將轉錄內容保留在歷史記錄中作為記錄。所有內容都留在你的 Mac 上。需要 macOS 14.2；翻譯需要 macOS 26。
#### improved
- 初始設定：文字清理現在在設定結束時預設關閉，讓你的第一次聽寫立即寫出。設定過程仍會示範它的作用；需要時可在「設定 › 格式」中開啟。
- 初始設定：開啟中文模式後，現在可以直接選擇簡體或繁體，並會根據介面語言預先選好。
- 設定：中文引擎現在會顯示其大小，位於中文模式下方和「儲存」中；關閉中文模式後可在「儲存」中刪除。
#### fixed
- 中文模式：聽寫可能中途停止寫入（有停頓時約 50 秒後，沒有停頓時幾分鐘後），之後說的內容全部遺失，而且沒有任何錯誤提示。長時間停頓前的句尾，或開頭一個詞後接著長時間靜音，也可能消失。現在聽寫不會再中途停止寫入。
- 中文模式：如果在最後幾個詞仍在轉寫時結束聽寫，文字結尾可能被截斷，或者較短的聽寫會被一段多餘的「Language French」取代。現在最後幾個詞總會完整轉寫。
- 中文模式：選擇「簡體」時，粵語聽寫的即時預覽會先顯示繁體字，最終文字才是簡體。現在預覽會依所選字體顯示。

## 0.4.1 · 2026-11-08
### en
#### improved
- Setup: the translation switch is a real switch; the Superpowers tab moves on only once each demo has fully played; the capsule menu has even margins on all sides.
- The bottom capsule stays bare at rest: the translation badge and the style symbol now show there only while you dictate. The island keeps its badge at rest.
- Setup: the translated dictation now has its own page, with the same look as the first dictation (language on top, key on the left, green when the text lands). The per-app style demo shows real app windows, a note, a Messages thread and a Mail draft, where the text arrives as Mumo transcribes it, and its app pills can be clicked.
#### fixed
- Setup: the dictation page no longer arrives with the key “already pressed” after testing the shortcut on the activation step, which made the first press do nothing.
- Setup, in English: the Email example of the per-app demo showed its internal name instead of the email.
- About: the credits now list the Chinese engine (Qwen3-ASR), Apple's translation engine, MLX, swift-transformers and Sparkle.
### fr
#### improved
- Configuration : l'interrupteur de traduction est un vrai interrupteur ; l'onglet Superpouvoirs n'enchaîne qu'une fois chaque démo jouée en entier ; le menu de la capsule a des marges égales de tous côtés.
- La capsule du bas reste nue au repos : le badge de traduction et le symbole du style n'y apparaissent plus que pendant la dictée. L'île garde son badge au repos.
- Configuration : la dictée traduite a désormais sa propre page, avec la même présentation que la première dictée (langue en tête, touche à gauche, vert quand le texte arrive). La démo du style par app montre de vraies fenêtres, une note, une conversation Messages et un brouillon Mail, où le texte arrive au fil de la transcription, et ses pilules d'app se cliquent.
#### fixed
- Configuration : la page de dictée n'arrive plus avec la touche « déjà appuyée » après un test du raccourci à l'étape Activation, qui rendait le premier appui muet.
- Configuration, en anglais : l'exemple E-mail de la démo par app affichait son nom interne au lieu de l'e-mail.
- À propos : les crédits mentionnent désormais le moteur chinois (Qwen3-ASR), le moteur de traduction d'Apple, MLX, swift-transformers et Sparkle.
### zh-Hans
#### improved
- 初始设置：翻译开关现在是真正的开关；“超能力”标签页会等每个演示完整播放后再切换；胶囊菜单四周的边距一致。
- 底部胶囊在待机时保持空白：翻译标记和风格符号现在只在听写时显示。灵动岛在待机时仍保留标记。
- 初始设置：翻译听写现在有自己的页面，外观与第一次听写一致（语言在顶部，按键在左侧，文字到达时变绿）。按应用设置风格的演示现在展示真实的应用窗口：备忘录、信息对话和邮件草稿，文字会随着 Mumo 的转录逐步出现，应用标签也可以点击。
#### fixed
- 初始设置：在“激活”步骤测试快捷键后，听写页面不再以“按键已按下”的状态出现（之前会导致第一次按键无效）。
- 初始设置（英文）：按应用演示中的“邮件”示例显示的是内部名称而不是邮件内容。
- 关于：致谢现在列出了中文引擎（Qwen3-ASR）、Apple 翻译引擎、MLX、swift-transformers 和 Sparkle。
### zh-Hant
#### improved
- 初始設定：翻譯開關現在是真正的開關；「超能力」標籤頁會等每個示範完整播放後再切換；膠囊選單四周的邊距一致。
- 底部膠囊在待機時保持空白：翻譯標記和樣式符號現在只在聽寫時顯示。動態島在待機時仍保留標記。
- 初始設定：翻譯聽寫現在有自己的頁面，外觀與第一次聽寫一致（語言在頂部，按鍵在左側，文字到達時變綠）。按 App 設定樣式的示範現在展示真實的 App 視窗：備忘錄、訊息對話和郵件草稿，文字會隨著 Mumo 的轉錄逐步出現，App 標籤也可以點按。
#### fixed
- 初始設定：在「啟用」步驟測試快速鍵後，聽寫頁面不再以「按鍵已按下」的狀態出現（之前會導致第一次按鍵無效）。
- 初始設定（英文）：按 App 示範中的「郵件」範例顯示的是內部名稱而不是郵件內容。
- 關於：致謝現在列出了中文引擎（Qwen3-ASR）、Apple 翻譯引擎、MLX、swift-transformers 和 Sparkle。

## 0.4.0 · 2026-11-08
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

## 0.3.0 · 2026-11-04
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

## 0.2.0 · 2026-09-17
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

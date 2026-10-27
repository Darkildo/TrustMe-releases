# История версий

Те же заметки, что и в [Releases](https://github.com/Darkildo/TrustMe-releases/releases), собранные в один файл. Новые версии сверху. Каждая запись: сначала по-русски, затем по-английски.


## 13.5.2 (2026-10-27)

Видео-стикеры в панели появляются быстрее и больше не теряют прозрачность.

**Что изменилось в 13.5.2**
- Видео-стикеры в панели и в редакторе набора появляются заметно быстрее: для миниатюры приложение готовит только первый кадр, а не весь стикер целиком.
- Видео-стикер больше не может стать полностью прозрачным посреди анимации, если в файле не хватает данных о прозрачности для отдельного кадра.
- Обновлены библиотека шифрования базы сообщений и другие компоненты ядра. Ваши данные остаются на месте: база открывается тем же ключом, ничего переносить не нужно.
- Обновлены криптографические библиотеки приложения. Ключи, контакты и переписка остаются прежними, совместимость с собеседниками на старых версиях сохраняется.

---

Video stickers in the panel appear faster and no longer lose their transparency.

**What's changed in 13.5.2**
- Video stickers in the panel and in the pack editor appear noticeably faster: for a thumbnail the app now prepares only the first frame instead of the whole sticker.
- A video sticker can no longer turn fully transparent in the middle of its animation when the file lacks transparency data for a single frame.
- The message database encryption library and other core components are updated. Your data stays where it is: the database opens with the same key, nothing needs to be migrated.
- The app's cryptographic libraries are updated. Your keys, contacts and conversations stay the same, and you can keep chatting with people on older versions.



## 13.5.1 (2026-10-27)

Анимированные стикеры больше не замирают и не пропадают, а новая плавная анимация переходов между экранами теперь в цветах вашей темы.

**Что изменилось в 13.5.1**
- В 13.5.0 при переходе между экранами в тёмной теме экран на мгновение становился белым. Теперь новая анимация перехода идёт на фоне текущей темы, без вспышки.
- Анимированные стикеры больше не застывают на первом кадре после просмотра набора или превью и когда в чате их много. Как только освобождается место, они снова оживают.
- Видео-стикеры не мигают пустым квадратом, когда останавливаются или снова запускаются. Если стикер не удалось открыть, вместо пустого места виден значок.
- Видео-стикеры в панели появляются быстрее: сначала готовятся те, что на экране, и только что отправленные в чате.
- Входящие стикеры до 512 КБ загружаются сами при любой сети, в том числе в роуминге и в режиме экономии трафика.
- Анимированные стикеры в формате WebP (например, из WhatsApp) распознаются и анимируются наравне с остальными.
- Анимированные стикеры занимают меньше памяти. При сбросе и тревожном коде из памяти стираются и уже показанные стикеры.

---

Animated stickers no longer freeze or disappear, and the new smooth screen transition now uses your theme's colors.

**What's changed in 13.5.1**
- In 13.5.0, the screen briefly turned white when moving between screens in the dark theme. The new transition now runs over the background of your current theme, without the flash.
- Animated stickers no longer get stuck on the first frame after you view a pack or a preview, or when a chat has many of them. They come back to life as soon as there is room.
- Video stickers no longer flash an empty square when they pause or start again. If a sticker can't be opened, you now see an icon instead of an empty space.
- Video stickers in the panel appear faster: the ones on screen and the ones you just sent in a chat are prepared first.
- Incoming stickers up to 512 KB download on their own on any network, including roaming and data saver mode.
- Animated WebP stickers (for example, from WhatsApp) are recognized and animated like the rest.
- Animated stickers use less memory. A reset or the duress code now also erases stickers already shown from memory.


## 13.5.0 (2026-10-26)

Приложение переведено на свежий Flutter и обновлённые библиотеки, а новые проверки помогли найти и исправить три скрытые ошибки в обработке сбоев.

**Что изменилось в 13.5.0**
- Приложение собрано на Flutter 3.47.8 и Dart 3.13.7 (было 3.44.2), последняя стабильная версия.
- Обновлены библиотеки уведомлений, видео, камеры, редактора изображений, Firebase и другие, всего около 150 пакетов.
- Исправлены три места, где ошибка при публикации аватара, пересылке сообщений или определении размеров медиа могла пройти мимо обработчика и оборвать операцию. Теперь такие ошибки перехватываются, а операция завершается корректно.
- Края скруглённых элементов интерфейса рисуются немного аккуратнее: так рендерит новый движок.

---

TrustMe now runs on a current Flutter with updated libraries, and the new checks helped find and fix three hidden bugs in error handling.

**What's changed in 13.5.0**
- The app is built with Flutter 3.47.8 and Dart 3.13.7 (previously 3.44.2), the latest stable release.
- Updated notification, video, camera, image editor, Firebase and other libraries, about 150 packages in total.
- Fixed three places where an error while publishing an avatar, forwarding messages or reading media dimensions could bypass its handler and break the operation. These errors are now caught and the operation finishes cleanly.
- Rounded edges in the interface are drawn slightly more cleanly, as rendered by the new engine.


## 13.4.2 (2026-10-26)

Стикеры стали безопаснее и легче, «Поделиться» на Android работает, а связь с нодой восстанавливается сама после любого обрыва.

**Что изменилось в 13.4.2**
- «Поделиться → TrustMe» на Android теперь открывает выбор чата и после ввода кода, и когда приложение было свёрнуто.
- После обрыва связи приложение переподключается к ноде само, даже если до этого работало долго. Раньше после 15 минут работы переподключение могло остановиться до возврата в приложение.
- Стикеры и наборы хранятся на устройстве в зашифрованном виде и удаляются вместе с данными при сбросе или тревожном коде.
- Испорченный стикер или архив набора больше не может уронить приложение: файлы проверяются до показа, а архив открывается только по нажатию.
- Наборы подписываются: обновить набор может только его автор. Чужой архив с тем же набором устанавливается отдельной копией. В карточке набора видно, от кого он.
- Набор, который вы отправляете по запросу, всегда уходит отдельным файлом.
- Стикеры в чатах и на панели работают плавнее: анимируются только те, что видны на экране.
- Порядок стикеров в своём наборе можно менять перетаскиванием. Программы чтения с экрана называют стикер по его эмодзи.

---

Stickers are safer and lighter, Share on Android works, and the connection to your node now recovers on its own after any drop.

**What's changed in 13.4.2**
- On Android, Share → TrustMe now opens the chat picker both after you enter your code and when the app was in the background.
- After a connection drop the app reconnects to the node on its own, even after a long session. Previously, after 15 minutes of use, reconnecting could stop until you returned to the app.
- Stickers and sticker packs are stored encrypted on the device and are erased together with your data on reset or with the duress code.
- A broken sticker or pack archive can no longer crash the app: files are checked before they are shown, and an archive is opened only when you tap it.
- Packs are signed: only the author can update a pack. Someone else's archive of the same pack installs as a separate copy. The pack card shows who it is from.
- A pack you send on request always goes as a separate file.
- Stickers in chats and in the panel run more smoothly: only the ones visible on screen are animated.
- You can reorder stickers in your own pack by dragging. Screen readers name a sticker by its emoji.


## 13.4.0 (2026-10-26)

Скрытые чаты, свои папки, отправка в TrustMe из других приложений и понятное ожидание, пока новый контакт подтвердит приглашение.

**Что изменилось в 13.4.0**
- Скрытые чаты. Любой чат можно убрать в скрытый раздел: он пропадает из списка, поиска и пересылки, а уведомления от него приходят без имени и текста. Раздел открывается своим кодом в настройках безопасности или в поиске. Неверный код открывает пустой раздел, поэтому со стороны не видно, есть ли там что-то.
- Свои папки чатов: до 10 вкладок рядом со «Всеми» и «Непрочитанными». Чат можно пометить непрочитанным, собеседник об этом не узнает.
- На Android TrustMe появился в меню «Поделиться» других приложений: фото, видео, файлы и текст отправляются в выбранный чат.
- После сканирования QR чат показывает, что контакт ещё не подтвердил приглашение. Писать уже можно, сообщения дойдут после подтверждения, а звонки станут доступны, когда контакт подтвердит. Неподтверждённое приглашение можно отменить.
- Новые заявки в контакты видны прямо над списком чатов.
- Тревожный код: если ввести его вместо обычного, все данные на устройстве стираются, а снаружи это выглядит как обычный вход.
- Связь с нодами стала надёжнее: соединение с контактом на другой ноде больше не обрывается, если подключение идёт медленно.

---

Hidden chats, your own folders, sharing into TrustMe from other apps, and a clear waiting state until a new contact confirms the invitation.

**What's changed in 13.4.0**
- Hidden chats. Any chat can be moved to a hidden section: it disappears from the chat list, search and forwarding, and its notifications arrive without a name or text. The section opens with its own code in security settings or in search. A wrong code opens an empty section, so nobody can tell whether anything is there.
- Your own chat folders: up to 10 tabs next to "All" and "Unread". You can mark a chat as unread, and the other person won't know.
- On Android, TrustMe now appears in the Share menu of other apps: photos, videos, files and text go to the chat you pick.
- After you scan a QR code, the chat shows that the contact hasn't confirmed the invitation yet. You can already write; messages arrive once they confirm, and calls become available after confirmation. An unconfirmed invitation can be cancelled.
- New contact requests now appear right above the chat list.
- Duress code: if you enter it instead of your usual code, all data on the device is erased, and it looks like a normal unlock.
- Connections between nodes are more reliable: a connection to a contact on another node no longer drops when it is slow to set up.


## 13.3.1 (2026-10-25)

Экран блокировки стал проще, а на компьютере звук больше не затихает во время звонка.

**Что изменилось в 13.3.1**
- Экран блокировки без лишнего: только точки кода, клавиатура и кнопка Face ID или отпечатка. Вход по коду, по паролю и после автоблокировки выглядят одинаково.
- Face ID или отпечаток предлагается сразу при открытии приложения.
- Сбросить аккаунт теперь можно по ссылке «Забыли PIN-код?» внизу экрана, а не долгим нажатием.
- Ошибка ввода кода показывается на одном месте, клавиатура больше не сдвигается.
- На Windows звук других приложений больше не затихает, когда вы в звонке или показываете экран со звуком.
- Когда вы удаляете своё сообщение с фото или видео, файл тоже удаляется с устройства.
- Приложение раз в неделю убирает файлы, которые уже нельзя открыть, и недокачанные остатки.

---

The lock screen is simpler, and on desktop other sounds no longer fade during a call.

**What's changed in 13.3.1**
- A cleaner lock screen: just the code dots, the keypad and a Face ID or fingerprint button. Unlocking with a code, a password or after auto-lock now looks the same.
- Face ID or fingerprint is offered as soon as the app opens.
- To reset your account, use the "Forgot your PIN?" link at the bottom of the screen instead of a long press.
- A wrong-code message always appears in the same place, so the keypad no longer jumps.
- On Windows, other apps no longer get quieter while you are in a call or sharing your screen with sound.
- When you delete your own message with a photo or video, the file is removed from your device too.
- Once a week the app clears out files that can no longer be opened and leftovers of unfinished downloads.


## 13.3.0 (2026-10-25)

Видео показываются в своих пропорциях, карта точнее считает дни, а звонки и медиа работают надёжнее.

**Что изменилось в 13.3.0**
- Видео в чате показываются в своих пропорциях: вертикальное — вертикально, широкое — широко. Видеокружки остаются кругами.
- Своё фото или видео сохраняется в «Избранное» быстрее и без лишней нагрузки на память. Скачанное медиа собеседника теперь сохраняется в «Избранное» вместе с файлом.
- Если медиа не открывается, пока приложение заблокировано, в сообщении видно, что нужно открыть приложение. После разблокировки медиа загружается само.
- Видео больше не перестаёт воспроизводиться при быстрой прокрутке чата.
- В групповом чате файл, который пропал с вашего устройства, приложение просит у участников, которые его получили.
- Звонок больше не обрывается из-за короткого сбоя связи в момент соединения.
- На компьютере выбранный микрофон больше не сбрасывается на системный во время звонка.
- Если в чате с защитой прошлых сообщений пришло сообщение без этой защиты, оно не принимается, и в чате появляется строка об этом.
- Карта: история перемещений правильно делит дни, в том числе в день перевода часов. При просмотре недели или месяца ползунок не уходит за выбранный день.
- Карта: в карточке контакта видно расстояние до него. Кнопка «Поделиться» в карточке сразу отмечает этого контакта, а на экране «Поделиться» видно превью карты с вашей позицией.

---

Videos keep their own proportions, the map counts days more accurately, and calls and media are more reliable.

**What's changed in 13.3.0**
- Videos in a chat keep their own proportions: a portrait video is shown upright and a wide one is shown wide. Video notes stay round.
- Saving your own photo or video to Saved Messages is faster and uses less memory. Downloaded media from a contact is now saved to Saved Messages together with its file.
- If media cannot be opened while the app is locked, the message now says to open the app. After unlocking, the media loads on its own.
- Videos no longer stop playing when you scroll a chat quickly.
- In a group chat, a file that is missing from your device is now requested from the members who received it.
- A short connection glitch while a call is connecting no longer ends the call.
- On desktop, the selected microphone is no longer reset to the system default during a call.
- In a chat with forward secrecy, a message that arrives without it is rejected, and the chat shows a line about it.
- Map: location history splits days correctly, including the day the clocks change. When viewing a week or a month, the slider stays within the selected day.
- Map: a contact's card shows the distance to them. The Share button in the card selects that contact right away, and the Share screen shows a map preview with your position.


## 13.2.0 (2026-10-24)

Видеокружки и голосовые теперь играют подряд, продолжаются в мини-плеере и не звучат одновременно.

**Что изменилось в 13.2.0**
- Кружки и голосовые идут цепочкой: когда сообщение доиграло, сразу начинается следующее, если это тоже кружок или голосовое. Цепочка продолжается, даже если вы вышли из чата.
- Мини-плеер: если прокрутить чат или выйти из него, кружок доигрывает в плавающем круге, а голосовое в плашке сверху. Круг можно перетащить в любой угол, поставить на паузу, закрыть или вернуться к сообщению в чате.
- Одновременно звучит что-то одно: голосовое останавливает кружок и наоборот, видео в галерее останавливает то, что играло в чате, а начало записи останавливает воспроизведение.
- Кружок встаёт на паузу при звонке и при сворачивании приложения. Прерванный кружок продолжается с того же места.
- Скорость воспроизведения общая для кружков и голосовых. Обычные видео всегда играют с обычной скоростью.
- На компьютере и планшете кружок при просмотре больше не растягивается на всю ширину чата.
- Если кружок не удалось воспроизвести, приложение сообщает об этом, а не молчит.

---

Video notes and voice messages now play one after another, keep playing in a mini player and never sound at the same time.

**What's changed in 13.2.0**
- Video notes and voice messages play as a chain: when one finishes, the next one starts right away if it is also a video note or a voice message. The chain keeps going even after you leave the chat.
- Mini player: if you scroll the chat or leave it, a video note keeps playing in a floating circle and a voice message in a bar at the top. You can drag the circle to any corner, pause it, close it or jump back to the message in the chat.
- Only one thing plays at a time: a voice message stops a video note and vice versa, a video in the gallery stops whatever was playing in the chat, and starting a recording stops playback.
- A video note pauses during a call and when the app is minimized. An interrupted video note resumes where it stopped.
- Playback speed is shared between video notes and voice messages. Regular videos always play at normal speed.
- On desktop and tablets a playing video note no longer stretches to the full width of the chat.
- If a video note cannot be played, the app now tells you instead of staying silent.


## 13.1.0 (2026-10-21)

Карту и геолокацию теперь можно выключить целиком, если они вам не нужны.

**Что изменилось в 13.1.0**
- Новый переключатель «Карта и геолокация» в настройках приватности. Когда он выключен, нет вкладки карты, приложение не просит доступ к геолокации и не записывает вашу позицию, а пункты «Локация» и «Точка» пропадают из вложений.
- При выключении активные трансляции геопозиции останавливаются. По желанию можно сразу отозвать у контактов доступ к истории локаций и стереть геоданные с устройства.
- Точки и трансляции, которые присылают собеседники, по-прежнему открываются на карте, отдельным экраном.
- Предупреждение о доступе к геолокации на карте больше не мигает и предлагает сразу выключить карту.

---

The map and location features can now be turned off entirely if you don't need them.

**What's changed in 13.1.0**
- A new "Map and location" switch in privacy settings. When it is off, there is no map tab, the app does not ask for location access or record your position, and "Location" and "Pin" disappear from attachments.
- Turning it off stops active live location shares. You can also revoke location history access from contacts and erase location data from the device right away.
- Locations and live shares sent by your contacts still open on a map, in a separate screen.
- The location access warning on the map no longer flickers and offers to turn the map off.


## 13.0.3 (2026-10-20)

Исправлена работа в фоне: уведомления и звонки снова доходят, когда приложение закрыто.

**Что изменилось в 13.0.3**
- Приложение снова просыпается по уведомлению, когда оно выгружено: новые сообщения приходят без открытия приложения.
- Входящий звонок снова можно принять с экрана блокировки.
- Завершение звонка из фона снова доходит до собеседника.

Ошибка появилась в 12.0: фоновая часть не могла открыть свои данные и сбрасывала их. Обновление исправляет это без действий с вашей стороны: достаточно один раз открыть приложение после установки.

---

Background operation is fixed: notifications and calls arrive again while the app is closed.

**What's changed in 13.0.3**
- The app wakes up on a notification again when it is not running: new messages arrive without opening the app.
- An incoming call can be answered from the lock screen again.
- Ending a call from the background reaches the other side again.

The bug was introduced in 12.0: the background part could not open its data and reset it. The update fixes this with no action needed: just open the app once after installing.


## 13.0.2 (2026-10-20)

Исправления после 13.0.1: свои устройства, перенос аккаунта, сопряжение по QR и голосовые сообщения.

**Что изменилось в 13.0.2**
- Удалённое своё устройство выходит из аккаунта сразу: сверка происходит при открытии приложения и по сигналу от других устройств.
- Перенос аккаунта на устройство, где уже был другой аккаунт: история и медиа приходят.
- Сопряжение по QR переживает кратковременный обрыв сети.
- Голосовое: запись больше не обрывается молча при звуке другого приложения; при звонке или прерывании она превращается в черновик.
- Длительность голосового сообщения теперь точная.

---

Fixes after 13.0.1: own devices, account transfer, QR pairing and voice messages.

**What's changed in 13.0.2**
- A removed own device now signs out of the account right away: the registry is checked when the app opens and on a signal from other devices.
- Transferring an account to a device that already had another account: history and media arrive.
- QR pairing survives a brief network drop.
- Voice: recording no longer stops silently when another app plays sound; on a call or interruption it becomes a draft.
- Voice message duration is now exact.


## 13.0.1 (2026-10-20)

Исправления после выхода 13.0: просмотр фото и видео, запуск приложения и исчезающие сообщения.

**Что изменилось в 13.0.1**
- Фото и видео, которые ещё не скачаны, открываются по тапу сразу в полноэкранном просмотре: видна миниатюра и прогресс, скачивание начинается само, а по готовности картинка становится чёткой без переоткрытия. Соседние фото можно листать, пока текущее грузится.
- В просмотре истёкшего файла есть кнопка «Попросить заново», у отозванного пометка «Файл удалён отправителем», при ошибке кнопка «Повторить».
- Исправлена ошибка при запуске, из-за которой журнал приложения не записывался до перезапуска.
- После исчезновения сообщения с медиа приложение больше не пытается читать удалённый файл.

---

Fixes after the 13.0 release: photo and video viewing, app startup and disappearing messages.

**What's changed in 13.0.1**
- Photos and videos that are not downloaded yet now open full-screen right away on tap: you see the thumbnail and progress, the download starts by itself, and the picture sharpens when ready without reopening. You can swipe to neighbouring photos while the current one is loading.
- The viewer offers "Ask again" for an expired file, shows "File deleted by sender" for a revoked one, and "Retry" after an error.
- Fixed a startup error that stopped the app log from being written until restart.
- After a disappearing message with media is removed, the app no longer tries to read the deleted file.


## 13.0.0 (2026-10-19)

Файлы в чатах теперь хранятся на вашей ноде и скачиваются по правилам, которые вы задаёте. Звонки получают временные учётки для ретрансляции от ноды.

**Что нового в 13.0**
- Фото, видео, голосовые и файлы загружаются на ноду и приходят получателю указателем. Крупные файлы больше не режутся на куски в чате: загрузка и скачивание идут отдельно, с понятным прогрессом.
- У каждого файла видно состояние: загружается, ждёт сети, скачивается, скачан, срок хранения истёк, отозван. Если файл истёк, можно попросить отправителя выложить его заново.
- «Настройки медиа»: автозагрузка по типу сети (Wi-Fi, мобильная, роуминг), срок хранения файлов на ноде и разрешение перевыкладывать файл по запросу.
- При отправке можно выбрать срок хранения файла на ноде.
- Свой файл можно отозвать у всех («Отозвать файл»).
- Видео и аудио проигрываются без расшифрованных копий на диске.
- Аватары контактов и групп приходят компактным указателем и не качаются в роуминге.
- Звонки: серверы и временные учётки для ретрансляции выдаёт нода; в долгом звонке учётки продлеваются без разрыва. Если нода серверы не выдаёт, остаётся прямое соединение через STUN.

**Важно**
- Файлы 13.0 несовместимы с 8.x и ранее: чтобы обмениваться медиа, обновитесь на обеих сторонах.
- Расшифрованные копии файлов из старых версий в кэше автоматически не удаляются; очистить их можно в «Хранилище».

---

Files in chats are now stored on your node and downloaded under rules you control. Calls get temporary relay credentials from the node.

**What's new in 13.0**
- Photos, videos, voice messages and files are uploaded to the node and delivered to the recipient as a pointer. Large files are no longer split into chunks inside the chat: upload and download run separately, with clear progress.
- Every file shows its state: uploading, waiting for network, downloading, downloaded, expired, revoked. If a file has expired, you can ask the sender to upload it again.
- "Media settings": auto-download by network type (Wi-Fi, mobile, roaming), how long files are kept on the node, and whether re-uploading on request is allowed.
- When sending, you can choose how long the file is kept on the node.
- You can revoke your own file for everyone ("Revoke file").
- Video and audio play without decrypted copies on disk.
- Contact and group avatars arrive as a compact pointer and are not downloaded while roaming.
- Calls: the node issues the servers and temporary relay credentials; in a long call the credentials are renewed without dropping the call. If the node issues no servers, the call falls back to a direct STUN connection.

**Important**
- 13.0 files are not compatible with 8.x and earlier: both sides must update to exchange media.
- Decrypted file copies left by older versions are not removed automatically; you can clear them in "Storage".


## 12.1.0 (2026-10-18)

Обновлены экраны своих устройств, нод и переноса аккаунта: статусы читаются с первого взгляда, а перенос идёт по понятным шагам.

**Что нового в 12.1**
- «Мои устройства»: у каждого устройства понятный статус: «Это устройство», «Подтверждено» или «Не подтверждено» с пояснением, что делать. Видно, сколько устройств из 8 уже занято. Удалённые устройства собраны в отдельный свёрнутый список. Своё устройство переименовывается тапом по нему.
- Пока устройство удаляется или переименовывается, на нём видно, что операция идёт.
- «Мои ноды»: роль ноды («Главная», «Авто», «Своя») и её состояние («На связи», «Нет сессии», «Недоступна», «Отключена») показаны отдельно. Длинные адреса не теряют порт. Размер пула и строгий режим выбираются переключателем. Кнопка «Добавить ноду» не пропадает при полном пуле, а объясняет, почему недоступна. Пока адрес новой ноды проверяется, повторно нажать кнопку нельзя.
- В настройках сервера сразу видно, сколько нод в пуле и какой строгий режим включён.
- Перенос аккаунта: сверху видно, на каком вы шаге: «Роль», «Код», «Передача», «Готово». Коды вводятся и показываются по ячейкам, их проще сверить. Виден размер файла переноса. После переноса со старого устройства можно сразу открыть «Мои устройства».
- Тексты переноса и сообщений об удалении аккаунта и прерванном переносе стали короче и понятнее.
- Диалоги стали шире и аккуратнее. Если подписи кнопок не помещаются в одну строку, кнопки встают друг под другом.

---

The screens for your devices, nodes and account transfer have been redesigned: statuses are clear at a glance, and the transfer goes through clear steps.

**What's new in 12.1**
- "My devices": every device has a clear status: "This device", "Verified", or "Not verified" with a hint on what to do. You can see how many of the 8 slots are used. Removed devices are grouped in a separate collapsed list. Rename your own device by tapping it.
- While a device is being removed or renamed, it shows that the operation is in progress.
- "My nodes": a node's role ("Primary", "Auto", "Custom") and its state ("Connected", "No session", "Unreachable", "Disabled") are shown separately. Long addresses keep their port visible. Pool size and strict mode are chosen with a switch. The "Add node" button no longer disappears when the pool is full: it explains why it is unavailable. While a new node address is being checked, the button cannot be pressed again.
- Server settings show right away how many nodes are in the pool and which strict mode is on.
- Account transfer: the top of the screen shows which step you are on: "Role", "Code", "Transfer", "Done". Codes are entered and shown cell by cell, so they are easier to compare. The transfer file size is shown. After a transfer, the old device can open "My devices" right away.
- Texts for the transfer and for the account-removed and interrupted-transfer messages are shorter and clearer.
- Dialogs are wider and tidier. When button labels do not fit on one line, the buttons stack.


## 12.0.1 (2026-10-17)

Промежуточная сборка для Android с исправлениями после 12.0.

**Что изменилось в 12.0.1**
- Потеря сети больше не обрывает соединение целиком: после восстановления сети приложение продолжает работать без перезапуска.
- Автоблокировка по времени срабатывает правильно после возврата из фона.
- Раздел защиты прошлых сообщений (Forward Secrecy) доступен в профиле.
- В «Моих устройствах» у подтверждённых устройств виден бейдж «Подтверждено».

---

An interim Android build with fixes after 12.0.

**What's changed in 12.0.1**
- Losing the network no longer drops the connection entirely: once the network is back, the app carries on without a restart.
- Timed auto-lock works correctly after returning from the background.
- The forward secrecy section is available in the profile.
- "My devices" shows the "Verified" badge on verified devices.


## 12.0.0 (2026-10-16)

Один аккаунт теперь работает на нескольких устройствах, а сообщения принимает пул из нескольких нод.

**Что нового в 12.0**
- До 8 устройств в одном аккаунте: телефон, планшет, компьютер. Контакты, чаты, переписка, группы, медиа, настройки и звонки синхронизируются между ними в зашифрованном виде. Новое устройство добавляется переносом с любого из уже подключённых.
- «Мои устройства»: список устройств аккаунта, переименование и удаление. Удалённое устройство выходит из аккаунта.
- «Мои ноды»: пул до 3 нод с приоритетом. Сообщения принимаются со всех включённых нод; если главная молчит, отправитель переходит к следующей. При добавлении ноды проверяется её отпечаток.
- Строгий режим: нода принимает сообщения только по очередям, которые вы выдали контактам. Режимы «Авто», «Вкл» и «Выкл».
- Усилена защита: ключ новых пар контактов выводится через HKDF, состав группы подписан владельцем, параметры Argon2id подняты до рекомендаций OWASP, удаление аккаунта стирает все данные, включая фоновые.

**Важно**
- 12.0 несовместима с 11.x: собеседники на старых версиях ваших сообщений не получат. Обновитесь сами и попросите обновиться контакты.
- Аккаунт при обновлении сохраняется. Перенос между 11.x и 12.0 не работает: обновите оба устройства.

---

One account now works on several devices, and messages are received by a pool of nodes.

**What's new in 12.0**
- Up to 8 devices in one account: phone, tablet, computer. Contacts, chats, messages, groups, media, settings and calls sync between them encrypted. A new device is added by a transfer from any device already in the account.
- "My devices": the list of the account's devices, rename and remove. A removed device signs out of the account.
- "My nodes": a pool of up to 3 nodes with priority. Messages are accepted on every enabled node; if the primary one is silent, the sender moves on to the next. A node's fingerprint is checked when it is added.
- Strict mode: a node accepts messages only through the queues you issued to your contacts. Modes "Auto", "On" and "Off".
- Hardening: the key of new contact pairs is derived via HKDF, group membership is signed by the owner, Argon2id parameters are raised to the OWASP recommendations, deleting the account wipes all data including the background parts.

**Important**
- 12.0 is incompatible with 11.x: contacts on older versions will not receive your messages. Update yourself and ask your contacts to update.
- Your account is kept when updating. A transfer between 11.x and 12.0 does not work: update both devices.


## 11.8.0 (2026-10-13)

Перенос аккаунта стал безопаснее, а в группах администраторы могут удалять чужие сообщения.

**Что нового в 11.8**
- Перенос аккаунта на новое устройство подтверждается кодом: новое устройство показывает 4 цифры, старое после их ввода показывает 6 цифр, их нужно ввести на новом. Так посторонний, увидевший QR, не сможет подсунуть чужой аккаунт. Перенесённый аккаунт теперь действительно становится аккаунтом нового устройства. Обновите TrustMe на обоих устройствах: старая и новая версии переносить друг другу не могут.
- Владелец и администраторы группы могут удалить чужое сообщение у всех. На его месте остаётся пометка «Сообщение удалено администратором». Админ не может удалить сообщения владельца и других админов. Участникам групп нужна эта же версия приложения.
- Для групп, созданных раньше, владелец один раз нажимает «Обновить права участников» в настройках группы, чтобы у остальных заработала модерация.
- Ответ на запрос прав больше не снимает уже выданные права. История геопозиции выдаётся только явно: диалог и окно создания QR прямо об этом предупреждают, а в правах контакта видно, что выдали вы.
- Выдача истории геопозиции у уже существующих контактов снята: после обновления её нужно выдать заново (ответом на запрос прав). Остальные права не тронуты. Перенос аккаунта с устройства на версии 11.7 и старше работает, но выдача истории геопозиции при этом снимается и её нужно выдать заново; чтобы выдача переносилась как есть, обновите оба устройства.
- Если перенос аккаунта прервался на середине, при следующем входе приложение скажет начать его заново. После успешного переноса остаётся одно действие: «Войти».
- Если данные на устройстве записаны более новой версией приложения, при входе появится просьба обновиться, а не ошибка кода доступа.

---

Account transfer is safer, and group admins can delete other people's messages.

**What's new in 11.8**
- Moving your account to a new device is now confirmed with a code: the new device shows 4 digits, the old one then shows 6 digits that you enter on the new device. Someone who merely saw the QR can no longer slip in a foreign account. The transferred account now really becomes the account of the new device. Update TrustMe on both devices: the old and new versions cannot transfer to each other.
- The group owner and admins can delete another member's message for everyone. A "Message deleted by an administrator" note stays in its place. An admin cannot delete messages of the owner or of other admins. Group members need this version of the app too.
- For groups created earlier, the owner taps "Refresh member permissions" once in the group settings so that moderation works for everyone else.
- Answering a permission request no longer removes rights you already granted. Location history is granted only explicitly: the dialog and the QR creation sheet warn about it, and a contact's permissions show what you granted.
- Location history grants for existing contacts have been cleared: after updating you need to grant it again (by answering a permission request). Other rights are untouched. Transfer from a device running app version 11.7 or older still works, but the location history grant is cleared and has to be granted again; to carry the grant over as is, update both devices.
- If an account transfer was interrupted midway, the next sign-in tells you to start it again. After a successful transfer the only action left is "Sign in".
- If the data on the device was written by a newer app version, sign-in asks you to update instead of reporting a wrong access code.


## 11.7.3 (2026-10-12)

Первая сборка, опубликованная в этом репозитории.

**Что нового в 11.7**
- Фото, видео и файлы на устройстве теперь шифруются по умолчанию, а их ключи открываются только после ввода PIN-кода или пароля.
- Пересылка больших файлов больше не загружает их целиком в память.
- Чат с защитой прошлых сообщений (FS) сам выходит из состояния «сломано», без ручного сброса.
- На компьютере новый экран ввода PIN-кода: можно вводить с клавиатуры, а экранная клавиатура стала компактнее.
- Заголовки разделов, чипсы и шторки оформлены единообразно; жест «назад» работает на Android 16.

---

First build published in this repository.

**What's new in 11.7**
- Photos, videos and files on the device are now encrypted by default; their keys unlock only after you enter your PIN or password.
- Forwarding large files no longer loads them into memory in full.
- A chat with forward secrecy (FS) now recovers from the "broken" state by itself, without a manual reset.
- Desktop: a new PIN entry screen with keyboard input and a compact on-screen keypad.
- Section headers, chips and sheets look consistent; the back gesture works on Android 16.

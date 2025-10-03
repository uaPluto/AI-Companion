# 🎧 SystemAudioToChatGPT – User Manual / Керівництво користувача / Руководство пользователя

---

## 🌐 Languages

- [English](#-user-manual-en)
- [Українська](#-керівництво-користувача-ua)
- [Русский](#-руководство-пользователя-ru)

---

# 🇬🇧 User Manual (EN)

## 📌 Overview
**SystemAudioToChatGPT** is a Windows application that:
- Captures **system audio** 
- Transcribes speech using **OpenAI STT (Whisper, GPT-4o-transcribe)**
- Sends transcribed text to **chat models (GPT-4o, GPT-4o-mini, etc.)**
- Takes **screenshots of selected areas** and sends them to OpenAI for analysis
- Supports **window protection mode** (hidden from Alt+Tab and screen capture)

It acts as an **AI Companion**: listens, transcribes, and helps you formulate responses.

---

## ⚙️ Requirements
- Windows 10/11 (x64)  
- .NET 6.0 Runtime  
- Installed `ffmpeg` (bundled)  
- Internet connection  
- OpenAI API Key (stored locally in encrypted form)  

---

## 🚀 Installation
1. Download the latest release from [Releases](./releases).  
2. Run the `.exe` installer.  
3. On first launch, enter and save your **API Key**.  
4. Check your audio input/output devices.  

---

## 🖥️ Main Window

### 🔑 API Key
- Enter and save OpenAI API Key  
- Stored at `%APPDATA%\SystemAudioToChatGPT\apikey.dat` in encrypted form  

### 🎛 Control Panel
- **Device Combo** — choose playback device (speakers)  
- **Mic Combo** — choose microphone  
- **Start** — start system audio capture  
- **Stop** — stop recording/session  
- **Clear Log** — clear log output  

### 🔊 Modes
1. **Realtime (UseRealtime)**  
   - Stream audio directly to OpenAI  
   - Receive real-time responses  
2. **STT+Chat (UseSttChat)**  
   - First transcription (Whisper / gpt-4o-transcribe)  
   - Then response from chat model (GPT-4o-mini, etc.)  
3. **Classic (UseNone)**  
   - Record to WAV/MP3  
   - Transcription happens after recording finishes  

### 📜 Log
- Logs all events: start/stop, model loading, errors, AI responses  

---

## 🖼️ Overlay Window (Screen Selection)
- Activated with **middle mouse button (wheel click)**  
- Draw a rectangle with the mouse  
- A PNG screenshot is created automatically  
- Screenshot is sent to OpenAI (Image API)  
- Response is shown in logs  
- Copy is also placed into clipboard  

---

## 🛡️ Protection Mode
- Toggle **Enable/Disable Protection**  
- Makes the window invisible to:  
  - Alt+Tab  
  - Screen capture (`SetWindowDisplayAffinity`)  
- When enabled, window becomes **TopMost** and hidden from taskbar  

---

## 🌐 Language
- Switch UI language with **LangCombo** 
- Supports Ukrainian and English 
- Logs: *“🌐 Language switched to: {code}”*  

---

## 📚 Usage Scenarios  
- 🎧 System audio → live assistance during calls/interviews  
- 🖼️ Screenshot → analyze text/data on screen  
- 🔄 Realtime → AI companion during negotiations  

---

## ❗ Troubleshooting
| Error | Cause | Solution |
|-------|-------|----------|
| ❌ API key missing | apikey.dat not set or deleted | Enter and save your key |
| ❌ ffmpeg Error | `ffmpeg.exe` not found in `ffmpeg` folder | Install ffmpeg or use bundled version |
| ⚠ Devices not found | No microphone/speakers | Check drivers and connections |
| ❌ SetWindowDisplayAffinity returned false | Windows < 10.2004 or unsupported GPU | Run without protection mode |

---

## 🔄 Updates
- On startup, app checks version against `min_supported`  
- If outdated → forced shutdown  
- Manual **Check for Updates** available in menu  

---

## 📬 Support
- Issues: [GitHub Issues](./issues)  
- Email: info@bandbi.site  

---

# 🇺🇦 Керівництво користувача (UA)

## 📌 Огляд
**SystemAudioToChatGPT** — це застосунок для Windows, який:
- Захоплює **системний звук** 
- Транскрибує мову через **OpenAI STT (Whisper, GPT-4o-transcribe)**
- Надсилає текст у **чат-моделі (GPT-4o, GPT-4o-mini тощо)**
- Робить **знімки вибраної області екрана** та надсилає їх до OpenAI для аналізу
- Підтримує **режим захисту вікна** (невидиме для Alt+Tab і захоплення екрана)

Додаток працює як **AI-компаньйон**: слухає, розшифровує та допомагає формулювати відповіді.

---

## ⚙️ Вимоги
- Windows 10/11 (x64)  
- .NET 6.0 Runtime  
- Встановлений `ffmpeg` (йде в комплекті)  
- Підключення до інтернету  
- API Key OpenAI (зберігається локально у зашифрованому вигляді)  

---

## 🚀 Встановлення
1. Завантажте останню версію з [Releases](./releases).  
2. Запустіть інсталятор `.exe`.  
3. Під час першого запуску введіть та збережіть свій **API-ключ**.  
4. Перевірте пристрої вводу/виводу.  

---

## 🖥️ Головне вікно

### 🔑 API Key
- Введення та збереження API-ключа OpenAI  
- Ключ зберігається у `%APPDATA%\SystemAudioToChatGPT\apikey.dat` у зашифрованому вигляді  

### 🎛 Панель керування
- **Device Combo** — вибір пристрою відтворення (динаміки)  
- **Mic Combo** — вибір мікрофона  
- **Start** — почати запис системного звуку  
- **Stop** — зупинка запису/сесії  
- **Clear Log** — очистити журнал  

### 🔊 Режими роботи
1. **Realtime (UseRealtime)**  
   - Потокова передача аудіо до OpenAI  
   - Отримання відповідей у реальному часі  
2. **STT+Chat (UseSttChat)**  
   - Спочатку транскрипція (Whisper / gpt-4o-transcribe)  
   - Потім — відповідь чат-моделі (GPT-4o-mini тощо)  
3. **Classic (UseNone)**  
   - Запис у WAV/MP3  
   - Транскрипція після завершення запису  

### 📜 Журнал
- Логує всі події: старт/стоп, завантаження моделей, помилки, відповіді AI  

---

## 🖼️ Overlay Window (Виділення екрану)
- Активується **середньою кнопкою миші (коліщатко)**  
- Виділіть прямокутник мишею  
- PNG-знімок створюється автоматично  
- Знімок надсилається до OpenAI (Image API)  
- Відповідь відображається у журналі  
- Копія також додається до буфера обміну  

---

## 🛡️ Режим захисту
- Перемикач **Enable/Disable Protection**  
- Робить вікно невидимим для:  
  - Alt+Tab  
  - захоплення екрана (`SetWindowDisplayAffinity`)  
- При активації вікно стає **TopMost** і приховується з панелі завдань  

---

## 🌐 Мова інтерфейсу
- Перемикач мов — **LangCombo**  
- Підтримка української та англійської мови інтерфейсу  
- У журналі: *“🌐 Language switched to: {код}”*  

---

## 📚 Сценарії використання
- 🎤 Мікрофон → транскрипція → відповідь AI  
- 🎧 Системний звук → підказки під час дзвінків/співбесід  
- 🖼️ Знімок екрану → аналіз тексту/даних  
- 🔄 Realtime → допомога під час перемовин  

---

## ❗ Помилки та рішення
| Помилка | Причина | Рішення |
|---------|---------|----------|
| ❌ API key відсутній | apikey.dat не задано або видалено | Введіть і збережіть ключ |
| ❌ ffmpeg Error | `ffmpeg.exe` не знайдено у папці `ffmpeg` | Встановіть ffmpeg або використайте вбудований |
| ⚠ Devices not found | Немає мікрофона/динаміків | Перевірте драйвери та підключення |
| ❌ SetWindowDisplayAffinity returned false | Windows < 10.2004 або непідтримувана GPU | Використовуйте без режиму захисту |

---

## 🔄 Оновлення
- При старті програма перевіряє версію з `min_supported`  
- Якщо застаріла → примусове завершення  
- У меню доступна ручна перевірка **Check for Updates**  

---

## 📬 Підтримка
- Issues: [GitHub Issues](./issues)  
- Email: support@bandbi.site  


--- 

# 🇷🇺 Руководство пользователя (RU)

## 📌 Обзор
**SystemAudioToChatGPT** — это Windows-приложение, которое:
- Захватывает **системный звук** 
- Транскрибирует речь через **OpenAI STT (Whisper, GPT-4o-transcribe)**
- Отправляет текст в **чат-модель (GPT-4o, GPT-4o-mini и др.)**
- Делает **скриншоты выделенной области** и отправляет их в OpenAI для анализа
- Поддерживает **режим защиты окна** (невидимость в Alt+Tab и захват экрана)

Приложение предназначено как **AI-компаньон**: слушает, расшифровывает и помогает формулировать ответы.

---

## ⚙️ Требования
- Windows 10/11 (x64)  
- .NET 6.0 Runtime  
- Установленный `ffmpeg` (идёт в комплекте)  
- Подключение к интернету  
- API Key OpenAI (сохраняется локально в зашифрованном виде)  

---

## 🚀 Установка
1. Скачайте последний релиз из [Releases](./releases).  
2. Запустите установщик `.exe`.  
3. При первом запуске введите свой **API-ключ** и сохраните.  
4. Проверьте устройства ввода/вывода.  

---

## 🖥️ Главное окно

### 🔑 API Key
- Ввод и сохранение API-ключа OpenAI  
- Ключ хранится в `%APPDATA%\SystemAudioToChatGPT\apikey.dat` в зашифрованном виде

### 🎛 Панель управления
- **Device Combo** — выбор устройства вывода (динамики)  
- **Mic Combo** — выбор микрофона  
- **Start (System)** — начать запись системного звука  
- **Stop** — остановка записи/сессии  
- **Clear Log** — очистка журнала  

### 🔊 Режимы работы
1. **Realtime (UseRealtime)**  
   - Потоковая передача аудио в OpenAI  
   - Получение ответов в реальном времени  
2. **STT+Chat (UseSttChat)**  
   - Сначала транскрипция (Whisper / gpt-4o-transcribe)  
   - Затем — генерация ответа чатом (GPT-4o-mini и др.)  
3. **Classic (UseNone)**  
   - Запись в WAV/MP3  
   - Отправка на транскрипцию после завершения  

### 📜 Журнал
- Все операции логируются: старт/стоп записи, загрузка моделей, ошибки, ответы моделей  

---

## 🖼️ Overlay Window (Выделение экрана)
- Активируется **средней кнопкой мыши (колёсиком)**  
- Мышью выделяется прямоугольная область  
- Автоматически создаётся PNG  
- PNG отправляется в OpenAI (Image API)  
- Ответ показывается в логах  
- Дополнительно: копия скриншота попадает в буфер обмена  

---

## 🛡️ Режим защиты
- Переключатель **Enable/Disable Protection**  
- Делает окно невидимым для:
  - Alt+Tab  
  - захвата экрана (API `SetWindowDisplayAffinity`)  
- При активации окно **становится TopMost** и скрывается из панели задач  

---

## 🌐 Язык интерфейса
- Поддержка смены языка через **LangCombo**  
- Поддержка украинского и английского языков интерфейса 
- В логи выводится сообщение: *“🌐 Language switched to: {код}”*  

---

## 📚 Сценарии использования
- 🎤 Запись микрофона → транскрипция → генерация ответа  
- 🎧 Запись системного звука → подсказки во время звонка/собеседования  
- 🖼️ Скриншот области → анализ текста/данных на экране  
- 🔄 Realtime → помощь во время переговоров  

---

## ❗ Ошибки и их решение
| Ошибка | Возможная причина | Решение |
|--------|------------------|----------|
| ❌ API key отсутствует | Не введён или удалён файл apikey.dat | Введите и сохраните ключ |
| ❌ ffmpeg Error | Нет `ffmpeg.exe` в папке `ffmpeg` | Установите ffmpeg или скачайте вместе с релизом |
| ⚠ Devices not found | Нет микрофона/динамиков | Проверьте драйверы и подключение |
| ❌ SetWindowDisplayAffinity returned false | Windows < 10.2004 или нет поддержки GPU | Используйте без защиты окна |

---

## 🔄 Обновления
- При старте приложение сверяет версию с `min_supported`  
- Если версия устарела → принудительное закрытие  
- В меню есть пункт **Check for Updates**  

---

## 📬 Поддержка
- Issues: [GitHub Issues](./issues)  
- Email: support@bandbi.site  


---

# Remote PC Management / Управление удаленными ПК

[![Windows](https://img.shields.io/badge/Platform-Windows-blue)](https://github.com/)
[![PowerShell](https://img.shields.io/badge/PowerShell-5.1+-green)](https://github.com/)
[![License](https://img.shields.io/badge/License-Free-orange)](https://github.com/)

---

## 🌍 Language / Язык

- [English](#english)
- [Русский](#русский)

---

## English

### 📋 Description

The program is designed for remote management of computers on a local network via WinRM (Windows Remote Management). It allows shutdown, reboot, sending text and voice messages to remote computers with credential storage.

### 🚀 Main Features

#### 1. Target PC Selection
| Feature | Description |
|---------|-------------|
| Manual IP input | Enter any IP address in the local network |
| IP history | Automatically saves used IPs |
| Availability check | Ping test before executing commands |

#### 2. Power Management
| # | Function | Description |
|---|----------|-------------|
| 1 | **Shutdown Now** | Instant remote PC shutdown |
| 2 | **Shutdown with Timer** | Shutdown after specified seconds |
| 3 | **Shutdown + Text** | Shutdown with text notification |
| 4 | **Shutdown + Voice** | Shutdown with voice warning |

#### 3. Message Sending
| # | Function | Description |
|---|----------|-------------|
| 5 | **Text Message** | Pop-up windows on remote PC |
| 6 | **Voice Message** | Speech synthesis via System.Speech |

#### 4. Credential Management
| # | Function | Description |
|---|----------|-------------|
| 7 | **Save Credentials** | Secure encrypted storage of logins and passwords |
| 8 | **Show Saved IPs** | View all saved addresses |
| 9 | **Delete Credentials** | Clear saved data for selected IP |

#### 5. Diagnostics
| # | Function | Description |
|---|----------|-------------|
| 10 | **Diagnostics** | Check PC availability, WinRM, port 5985 |

#### 6. Interface
| Feature | Description |
|---------|-------------|
| 🌐 Bilingual | Russian/English interface |
| 🎨 Colored output | Emoji indicators for status |
| 📊 Progress bar | Visual feedback for operations |
| 🔒 Fixed window | No resizing, clean layout |

### 📖 User Guide

#### 🔧 Initial Setup

1. **Run the program** as administrator (required for WinRM)
2. **Select language** in the top-right corner
3. **Enter IP address** of target computer
4. **Save credentials** (item 7) - enter login and password for remote PC

#### 💻 Power Management

<details>
<summary><b>Item 1: Shutdown Now</b></summary>

- Click "1. SHUTDOWN NOW" button
- Command executes immediately
- Result: ✅ or ❌ with error message
</details>

<details>
<summary><b>Item 2: Shutdown with Timer</b></summary>

1. Enter seconds until shutdown (e.g., 30, 60, 120)
2. Click OK
3. Command executes after specified time
</details>

<details>
<summary><b>Item 3: Shutdown + Text</b></summary>

1. Enter time in seconds
2. Enter warning text
3. Message window appears on remote PC
4. PC shuts down after specified time
</details>

<details>
<summary><b>Item 4: Shutdown + Voice</b></summary>

1. Enter time in seconds
2. Enter text for voice
3. Voice message plays on remote PC
4. PC shuts down after specified time
</details>

#### 💬 Sending Messages

<details>
<summary><b>Item 5: Text Message</b></summary>

1. Enter message text
2. Pop-up window appears on remote PC for 30 seconds
</details>

<details>
<summary><b>Item 6: Voice Message</b></summary>

1. Enter text for voice
2. Voice message plays on remote PC using text-to-speech
</details>

#### 🔐 Credential Management

<details>
<summary><b>Item 7: Save Credentials</b></summary>

- Enter login and password for remote PC
- Data is encrypted and saved in `C:\temp\`
- Format: `remote_cred_192_168_1_100.xml`
</details>

<details>
<summary><b>Item 8: Show Saved IPs</b></summary>

- Displays all IPs with saved credentials
- Shows list of files in `C:\temp\`
</details>

<details>
<summary><b>Item 9: Delete Credentials</b></summary>

- Deletes saved data for current IP
- Requires confirmation before deletion
</details>

#### 🔍 Diagnostics

<details>
<summary><b>Item 10: Diagnostics</b></summary>

Performs three checks:
1. **Ping test** - basic network availability
2. **WinRM test** - remote management service
3. **Port 5985 test** - WinRM default port

Output example:

CONNECTION DIAGNOSTICS
════════════════════════════════════════

PING TEST:
✅ Computer 192.168.1.100 is online

WINRM TEST:
✅ WinRM is available

PORT 5985 TEST:
✅ Port 5985 is open

✅ DIAGNOSTICS COMPLETE

</details>

#### 🧹 Clear Output

| Button | Function |
|--------|----------|
| **CLEAR OUTPUT** | Clears the output window |

### ⚠️ Important Notes

1. **Administrator Rights** - program requires administrator privileges
2. **WinRM** - target PC must have WinRM configured (port 5985)
3. **Firewall** - port 5985 must be open on target PC's firewall
4. **Credentials** - stored encrypted, accessible only to current user
5. **Availability** - program checks PC availability before executing commands

### 📁 File Structure

C:\temp

├── remote_cred_192.168.1.100.xml # Encrypted credentials for IP

├── remote_cred_192.168.1.120.xml # Encrypted credentials for IP

└── ...


### 🔧 Troubleshooting

| Error | Solution |
|-------|----------|
| ❌ Computer is offline | Check if target PC is turned on and network connection |
| ❌ WinRM is unavailable | Run on target PC: `winrm quickconfig` |
| ❌ Port 5985 is closed | Open port in target PC's firewall |
| ⚠️ Credentials not found | Save credentials via item 7 first |
| ❌ Execution error | Check if credentials are correct |

---

## Русский

### 📋 Описание программы

Программа предназначена для удаленного управления компьютерами в локальной сети через WinRM (Windows Remote Management). Позволяет выполнять выключение, перезагрузку, отправку текстовых и голосовых сообщений на удаленные компьютеры с сохранением учетных данных.

### 🚀 Основные функции

#### 1. Выбор целевого ПК
| Функция | Описание |
|---------|----------|
| Ручной ввод IP | Любой IP-адрес в локальной сети |
| История IP | Автоматическое сохранение использованных адресов |
| Проверка доступности | Ping-тест перед выполнением команд |

#### 2. Управление питанием
| # | Функция | Описание |
|---|---------|----------|
| 1 | **Выключить сейчас** | Мгновенное выключение |
| 2 | **Выключить с таймером** | Выключение через N секунд |
| 3 | **Выключить + текст** | Выключение с текстовым уведомлением |
| 4 | **Выключить + голос** | Выключение с голосовым предупреждением |

#### 3. Отправка сообщений
| # | Функция | Описание |
|---|---------|----------|
| 5 | **Текстовое сообщение** | Всплывающие окна на удаленном ПК |
| 6 | **Голосовое сообщение** | Синтез речи через System.Speech |

#### 4. Управление учетными данными
| # | Функция | Описание |
|---|---------|----------|
| 7 | **Сохранить учетные данные** | Безопасное хранение логинов и паролей |
| 8 | **Список сохраненных IP** | Просмотр всех сохраненных адресов |
| 9 | **Удалить учетные данные** | Очистка данных для выбранного IP |

#### 5. Диагностика
| # | Функция | Описание |
|---|---------|----------|
| 10 | **Диагностика** | Проверка доступности ПК, WinRM, порта 5985 |

#### 6. Интерфейс
| Функция | Описание |
|---------|----------|
| 🌐 Двуязычный | Русский/английский интерфейс |
| 🎨 Цветной вывод | Эмодзи-индикаторы статуса |
| 📊 Прогресс-бар | Визуальная обратная связь |
| 🔒 Фиксированное окно | Нет изменения размера |

### 📖 Инструкция по использованию

#### 🔧 Первоначальная настройка

1. **Запустите программу** от имени администратора (требуется для WinRM)
2. **Выберите язык** в правом верхнем углу
3. **Введите IP-адрес** целевого компьютера
4. **Сохраните учетные данные** (пункт 7) - введите логин и пароль

#### 💻 Управление питанием

<details>
<summary><b>Пункт 1: Выключить сейчас</b></summary>

- Нажмите кнопку "1. ВЫКЛЮЧИТЬ СЕЙЧАС"
- Команда выполнится мгновенно
- Результат: ✅ или ❌ с описанием ошибки
</details>

<details>
<summary><b>Пункт 2: Выключить с таймером</b></summary>

1. Введите количество секунд (например, 30, 60, 120)
2. Нажмите OK
3. Команда выполнится через указанное время
</details>

<details>
<summary><b>Пункт 3: Выключить + текст</b></summary>

1. Введите время в секундах
2. Введите текст предупреждения
3. На удаленном ПК появится окно с сообщением
4. Через указанное время ПК выключится
</details>

<details>
<summary><b>Пункт 4: Выключить + голос</b></summary>

1. Введите время в секундах
2. Введите текст для озвучки
3. На удаленном ПК прозвучит голосовое сообщение
4. Через указанное время ПК выключится
</details>

#### 💬 Отправка сообщений

<details>
<summary><b>Пункт 5: Текстовое сообщение</b></summary>

1. Введите текст сообщения
2. На удаленном ПК появится всплывающее окно на 30 секунд
</details>

<details>
<summary><b>Пункт 6: Голосовое сообщение</b></summary>

1. Введите текст для озвучки
2. На удаленном ПК прозвучит голосовое сообщение
</details>

#### 🔐 Управление учетными данными

<details>
<summary><b>Пункт 7: Сохранить учетные данные</b></summary>

- Введите логин и пароль от удаленного ПК
- Данные сохраняются в зашифрованном виде в `C:\temp\`
- Формат: `remote_cred_192_168_1_100.xml`
</details>

<details>
<summary><b>Пункт 8: Список сохраненных IP</b></summary>

- Показывает все IP с сохраненными данными
- Отображает список файлов в `C:\temp\`
</details>

<details>
<summary><b>Пункт 9: Удалить учетные данные</b></summary>

- Удаляет сохраненные данные для текущего IP
- Требует подтверждения перед удалением
</details>

#### 🔍 Диагностика

<details>
<summary><b>Пункт 10: Диагностика</b></summary>

Выполняет три проверки:
1. **Ping-тест** - базовая доступность по сети
2. **WinRM тест** - служба удаленного управления
3. **Порт 5985** - стандартный порт WinRM

Пример вывода:

ДИАГНОСТИКА ПОДКЛЮЧЕНИЯ
════════════════════════════════════════

ПРОВЕРКА СВЯЗИ:
✅ Компьютер 192.168.1.100 доступен

ПРОВЕРКА WINRM:
✅ WinRM доступен

ПРОВЕРКА ПОРТА 5985:
✅ Порт 5985 открыт

✅ ДИАГНОСТИКА ЗАВЕРШЕНА

</details>

#### 🧹 Очистка вывода

| Кнопка | Функция |
|--------|---------|
| **ОЧИСТИТЬ ВЫВОД** | Очищает окно вывода |

### ⚠️ Важные замечания

1. **Права администратора** - программа требует запуска от имени администратора
2. **WinRM** - на целевом ПК должен быть настроен WinRM (порт 5985)
3. **Брандмауэр** - порт 5985 должен быть открыт в брандмауэре целевого ПК
4. **Учетные данные** - сохраняются в зашифрованном виде, доступны только текущему пользователю
5. **Доступность** - программа проверяет доступность ПК перед выполнением команд

### 📁 Структура файлов

C:\temp

├── remote_cred_192.168.1.100.xml # Зашифрованные данные для IP

├── remote_cred_192.168.1.120.xml # Зашифрованные данные для IP

└── ...


### 🔧 Устранение неполадок

| Ошибка | Решение |
|--------|---------|
| ❌ Компьютер не отвечает | Проверьте, включен ли ПК и сетевое соединение |
| ❌ WinRM недоступен | Выполните на целевом ПК: `winrm quickconfig` |
| ❌ Порт 5985 закрыт | Откройте порт в брандмауэре целевого ПК |
| ⚠️ Данные не найдены | Сохраните учетные данные через пункт 7 |
| ❌ Ошибка выполнения | Проверьте правильность логина/пароля |

---

## 📝 Version History / История версий

- Initial release / Первый релиз
- Basic remote management functions / Базовые функции удаленного управления
- Bilingual interface / Двуязычный интерфейс
- Credential management / Управление учетными данными
- Connection diagnostics / Диагностика подключения

---

## 👨‍💻 Author / Автор

Created for remote PC management in local networks.  
Создано для удаленного управления ПК в локальных сетях.

---

## 📄 License / Лицензия

Free for personal and educational use.  
Бесплатно для личного и образовательного использования.

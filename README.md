# Заметки на каждый день.

Набор скриптов для работы с API [Evernote](http://evernote.com/) сервисом по созданию заметок, записок, календарей. Нужно [зарегистрироваться](https://www.evernote.com/Registration.action?referralSpecifier=mktgrepack_en_oo_web_cpl_V00), получить [персональный токен](https://dev.evernote.com/doc/articles/authentication.php#temporary_token_request).

### Запуск

Python 2.7 или Python 3.3 и выше должен быть установлен.

Для python 2.7 __возможны проблемы с запуском рекомендуется использовать Python 3.3 и выше.__

```bash
pip install -r requirements.txt
```
Для python 3.3 используйте [это](https://github.com/evernote/evernote-sdk-python3) и

```bash
pip install -r requirements.txt
```

### Скрипт add_note2journal.py

Создает заметку или notebook, принимает аргумент в виде даты формата `YYYY-MM-DD`

Пример запуска:

```bash
python add_note2journal.py 2022-01-10

```

### Скрипт config.py.

Скрипт настройки использует переменные окружения.

Пример: `.env`

```
EVERNOTE_CONSUMER_KEY="Персональный ключ"
EVERNOTE_CONSUMER_SECRET="Секретный ключ"
EVERNOTE_PERSONAL_TOKEN="Ваш персональный токен к API"
JOURNAL_TEMPLATE_NOTE_GUID="GUID заметки"
JOURNAL_NOTEBOOK_GUID="GUID notebook"
INBOX_NOTEBOOK_GUID="входяший GUID notebook"
```

### Скрипт list_notebooks.py.

Скрипт отображает имена(GUID) и количество созданных заметок на вашем [Evernote](http://evernote.com/).

Запуск:

```bash
python list_notebooks.py
```

### Скрипт dump_inbox.py

Создает временную базу с данными заметок из вашего [Evernote](http://evernote.com/), также принимает аргумент в виде числа определяющего количество заметок выведенных на экран, по умолчанию 10.

Пример запуска:

```bash
python dump_inbox.py 1
```
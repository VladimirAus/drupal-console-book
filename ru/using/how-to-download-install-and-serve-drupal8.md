# Как скачать, установить и запустить Drupal 8

Проще всего установить Drupal 8 используя команду `chain` с опцией `--file=~/.console/chain/quick-start.yml` следующим образом:

```
$ drupal chain --file=~/.console/chain/quick-start.yml
```
> ВНИМАНИЕ: Файл `~/.console/chain/quick-start.yml` доступен после инициализации Drupal Console командой `drupal init`.

Команда `chain` автоматизирует выполнение списка команд, прописанных в YAML файле. В файле прописаны имена, опции и аргументы для каждой команды. Команды выполняются по мере появления в файле.

Код файла `~/.console/chain/quick-start.yml`:

```
commands:
  - command: site:new
    arguments:
      directory: drupal8.dev
      version: 8.0.2
  - command: site:install
    options:
        langcode: en
        db-type: sqlite
        db-file: sites/default/files/.ht.sqlite
        site-name: 'Drupal 8 Quick Start'
        site-mail: admin@example.com
        account-name: admin
        account-mail: admin@example.com
        account-pass: admin
        generate-inline: true
    arguments:
        profile: standard
  - command: server
```

Вышеуказанный файл скачивает и устанавливает Drupal с поддержкой базы данных SQLite и запускает вебсайт через встроенный PHP сервер по адресу 127.0.0.1:8088.

YAML файл можно модифицировать по вашему усмотрению. К примеру, можно добавить дополнительные модули (команда `module:download`), установить скачанные модули (команда `module:install`), импортировать файлы конфигурации (команда `config:import`), восстановить базу данных (команда `database:restore`) или любую команду Drupal Console.

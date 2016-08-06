# Установка на Windows ОС

Существует два варианта установки Drupal Console на Windows ОС: используя приложение Git Bash или используя коммандную строку Windows ОС. Мы рекомендуем приложение Git Bash из пакета приложений Git for Windows (ранее msysgit), так как это единственный вариант для запуска Drupal Console без префикса `php`.

## Используя окно команадной строки Git Bash:

Чтобы установить Drupal Console в окне команадной строки Git Bash, скачайте и установите следующие приложения:

* [Git для Windows](https://git-for-windows.github.io/)
* [Composer](https://github.com/composer/windows-setup)
* [PHP для Windows](http://windows.php.net/download/)
* [sqlite-tools-win32-x86](https://www.sqlite.org/download.html)

### Обновите переменную PATH операционной системы

Посте установки добавьте путь к приложениям `php.exe` и `sqlite3.exe` в переменную PATH операционной системы.
К примеру, если "PHP для Windows" установлено в директории "C:\php", а "sqlite-tools-win32-x86" - в директории "C:\sqlite", переменная PATH операционной системы может быть обновлена следующим образом через окно командной строки:

```
SETX /M PATH "%PATH%;C:\php;C:\sqlite"
```

### Конфигурация php.ini

Приложение Drupal Console использует несколько PHP расширений, которые следует с в php.ini.

```
extension=php_gd2.dll
extension=php_pdo_sqlite.dll
```

Если есть необходимость использовать другие языки, мы рекомендуем расширений следующие расширения.

```
extension=php_intl.dll
extension=php_mbstring.dll
```

#### Установка сертификата

Установите сертификат, прилогаемый с приложением Git для Windows следующим образом

```
curl.cainfo = C:\Program Files\Git\usr\ssl\certs\ca-bundle.crt;
```

## Установить Drupal Console глобано, используя composer:

```
$ composer global require drupal/console:@stable
```

#### Теперь Drupal Console можно запустить следующим образом:

```
$ drupal chain --file="C:\Users\username\.console\chain\quick-start.yml"
```

**ВНИМАНИЕ:** Путь к файлу должен быть в стиле Windows ОС для опции `file`.

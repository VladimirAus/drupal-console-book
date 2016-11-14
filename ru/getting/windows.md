# Установка на Windows ОС

Существует два варианта установки Drupal Console на Windows ОС: 
используя приложение Git Bash или используя коммандную строку Windows ОС. 
Мы рекомендуем приложение Git Bash из пакета приложений Git for Windows 
(ранее msysgit), так как это единственный вариант для запуска Drupal Console 
без префикса `php`.

## В окне команадной строки приложения Git Bash:

Для работы с Drupal Console в окне команадной строки приложения Git Bash установите следующие приложения:

* [Git для Windows](https://git-for-windows.github.io/)
* [Composer](https://github.com/composer/windows-setup)
* [PHP для Windows](http://windows.php.net/download/)
* [sqlite-tools-win32-x86](https://www.sqlite.org/download.html)

### Обновите переменную `PATH` операционной системы:

Добавьте php.exe и sqlite3.exe в переменную `PATH` операционной системы.
Например, если вы установили "PHP For Windows" в папку "C:\php", 
а приложение "sqlite-tools-win32-x86" в папку "C:\sqlite", 
переменная `PATH` операционной системы может быть обновлена следующим образом
в командной строке:

```
SETX /M PATH "%PATH%;C:\php;C:\sqlite"
```

### Конфигурация php.ini

Drupal Console require some extensions. please enable these extensions in your php.ini.

```
extension=php_gd2.dll
extension=php_pdo_sqlite.dll
extension=php_curl.dll
extension=php_openssl.dll
```

We recommend to enable the following extensions to enable you to use your own language.

```
extension=php_intl.dll
extension=php_mbstring.dll
```

#### Конфигурация сертификатов

put certificate information provided by Git for Windows.

```
curl.cainfo = C:\Program Files\Git\usr\ssl\certs\ca-bundle.crt;
```

### Глобальная установка Drupal Console с помощью приложения composer:

```
$ composer global require drupal/console:@stable
```

### Теперь Drupal Console можно запускать:

```
$ drupal
```

or execute one of the chain available, to execute a quick install execute the following command

```
$ drupal chain --file="C:\Users\username\.console\chain\quick-start.yml"
```

**ВНИМАНИЕ:** You have to provide "Windows-style" path for `file` option.

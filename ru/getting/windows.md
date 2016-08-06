# Установка на Windows ОС
Существует два варианта установки Drupal Console на Windows ОС: используя приложение Git Bash или используя коммандную строку Windows ОС. Мы рекомендуем приложение Git Bash из пакета приложений Git for Windows (ранее msysgit), так как это единственный вариант для запуска Drupal Console без префикса `php`.

## Используя команду curl в окне команадной строки Git Bash:
```
$ curl https://drupalconsole.com/installer -L -o drupal.phar
```
## ИЛИ запуск через окно команадной строки Windows ОС:
```
$ php -r "readfile('https://drupalconsole.com/installer');" > drupal.phar
```

Теперь можно запустить Drupal Console при условии что `php.exe` приписал в переменной PATH операционной системы.

## Запуск Drupal Console:

```
$ php drupal.phar
```

Чтобы запустить Drupal Console без префикса `php` в окне команадной строки Git Bash, переименуйте файл `drupal.phar` в `drupal` и скопируйте его в директорию к файлу `php.exe`.

#### Теперь Drupal Console можно запустить следующим образом:
```
$ drupal
```

**ВНИМАНИЕ:** Имя файла `drupal` - всего лишь псевдоним (алиас) и файлу можно присвоить любое имя.

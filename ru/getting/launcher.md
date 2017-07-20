# Установка пускового файла Drupal Console

С помощью командного приложения curl:

```
curl https://drupalconsole.com/installer -L -o drupal.phar
mv drupal.phar /usr/local/bin/drupal
chmod +x /usr/local/bin/drupal
```

ИЛИ если командное приложение curl не установлено

```
php -r "readfile('https://drupalconsole.com/installer');" > drupal.phar
```

## Обновление пускового файла Drupal Console

```
drupal self-update
```

## Запуск пускового файла Drupal Console

```
$ drupal
```

Пусковой файл Drupal Console можно запустить из папки, где установлен Drupal
или указав флаг `--root=/путь/к/drupal8.dev`.

**ВНИМАНИЕ:** Имя файла `drupal` - всего лишь псевдоним (алиас) и файлу 
можно присвоить любое имя.

======
======
======

# Установка: phar файл 

Скачать самую свежую версию Drupal Console можно со страницы:

https://github.com/hechoendrupal/drupal-console

Убедитесь, что вы скачиваете последнюю версию файла console.phar

=======

# Стандартная инсталляция Drupal Console
При стандартной инсталляции Drupal Console, запущенной из дериктории проекта, все файлы будет скачаны на ваш компьютер. Drupal Console может быть установлена 

## С помощью curl:
```
$ curl https://drupalconsole.com/installer -L -o drupal.phar
```
## Или если curl не установлен:
```
$ php -r "readfile('https://drupalconsole.com/installer');" > drupal.phar
```

## После чего Drupal Console можно использовать, выполнив команду:
```
$ php drupal.phar
```

Файл drupal.phar может быть помещен в любую директорию на компьютере. Приложение можно зарегистрировать глобально (для дальнейшего обращения), обновив переменную PATH операционной системы. На *nix системах (Unix, Linux, MacOS) приложение можно использовать без обращения к php.

### Переместите приложение в директорию, прописанную в переменной PATH операционной системы:
```
$ mv drupal.phar /usr/local/bin/drupal
```

### Убедитесь, что у вас есть привелегии запуска приложения:
```
$ chmod +x /usr/local/bin/drupal
```

======

# Обновления проекта
Drupal 8 находится в постоянной разработке, соответсвенно и Drupal Console. Самый легкий способ обновления Drupal Console - это использование команды `self-update`.

## В зависимости от метода установки:

### Drupal Console установлен глобально (и переименован в "drupal"):
```
$ drupal self-update
```

### Drupal Console установлен глобально (c помощью Composer):
```
$ composer global update drupal/console:@stable
```

### Drupal Console установлен локально (файл console.phar в дериктории проекта):
```
$ php console.phar self-update
```


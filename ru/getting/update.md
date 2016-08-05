# Обновления проекта
Drupal 8 is under heavy development, to keep in sync with the latest changes. The easiest and recommended way of updating Drupal Console is using the self-update command.
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


# Как скопировать конфигурационные файлы

Перым делом после инсталации Drupal Console запустите команду `init`. `drupal init` скопирует конфигурационные настройки в директорию `~/.console/`. Изменить конфигурационные настройки можно через флаг `--override`
 
 ```
 $ drupal init [--override]
 ```
 
### Список файлов, которые копирует `init`.
```
 ~/.console/ 
 ├── aliases.yml 
 ├── chain
 │   ├── quick-start.yml
 │   └── sample.yml 
 ├── config.yml 
 ├── console.rc 
 ├── drupal.fish 
 └── sites 
     └── sample.yml 
```

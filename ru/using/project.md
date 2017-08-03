# Использование проекта

Два типа команд Drupal Console

1. **Доступные глобально:** Команды, которые можено запустить из любой папки.
2. **Доступные отдельному сайту:** Команды, которые можено запустить только из папки с Drupal.

### Запуск Drupal Console из любой папки 

Drupal Console можно запустить из любой папки используя опцию `--root` option to define the Drupal root to be use in the command execution. 

```
drupal --root=/var/www/drupal8.dev cr all
```

**NOTE:** Possible messages when executing Drupal Console outside a Drupal site root and no `--root` option provided.

When running the project outside of a Drupal 8 site root, the following message will be shown.  
> In order to list all of the available commands, you should run this inside a drupal root directory.

When running the project within of a Drupal 8 site root, but site is not yet installed, the following message will be shown.
> In order to list all of the available commands you should install drupal first.

If you already have an existing Drupal 8 site and have installed the global Launcher using the instructions in [2.2](../getting/launcher.md), you will still need to install it into the Drupal site using instructions at [2.1](../getting/composer.md) section.

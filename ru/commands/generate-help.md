# generate:help
Generate an implementation of hook_help()

**Usage:**
```
drupal generate:help [options]
gh
```

## Available options
Option | Details
-------|-------------
--module | Имя модуля.
--description | Module description

## Examples
* Generate a hook help specifying the module name and the description
```
drupal generate:help  \
  --module="modulename"  \
  --description="My Awesome Module"
```

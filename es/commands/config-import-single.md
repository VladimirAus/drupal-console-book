# config:import:single
Importar la configuración seleccionada.

**Usage:**
```
drupal config:import:single [options]
cis
```

## Available options
Option | Details
-------|-------------
--file | The file(s) name or file(s) absolute path to import
--directory | commands.config.import.arguments.directory

## Examples
* Providing a file option using full path.
```
drupal config:import:single \
  --file="/path/to/file/block.block.default_block.yml"
```
* Providing file and directory options
```
drupal config:import:single  \
  --file="block.block.default_block.yml" \
  --directory="/path/to/directory"
```

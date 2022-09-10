# Install Drush On Windows

## Remove drush globally

```shell
composer global remove drush/drush
```

## Installation - Phar

1. Download latest stable release via CLI (code below) or browse to https://github.com/drush-ops/drush-launcher/releases/latest.

    OSX:
    ```Shell
    curl -OL https://github.com/drush-ops/drush-launcher/releases/latest/download/drush.phar
    ```

    Linux:

    ```Shell
    wget -O drush.phar https://github.com/drush-ops/drush-launcher/releases/latest/download/drush.phar
    ```
1. Make downloaded file executable: `chmod +x drush.phar`
1. Move drush.phar to a location listed in your `$PATH`, rename to `drush`: 

    ```Shell
    mv drush.phar "C:\Users\akbar\AppData\Roaming\Drush"
    ```
    
1. Windows users: create a drush.bat file in the same folder as drush.phar with the following lines. This gets around the problem where Windows does not know that the `drush` file is associated with `php`:
   
    ``` Bat
    @echo off
    php "%~dp0\drush.phar" %*
    ```

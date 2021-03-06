##Общие параметры (минимальные)

- версия веб-сервера: Apache 2.2
- включена обработка .htaccess (mod_rewrite)
- версия PHP 5.4 и выше
- **версия PHP 5.3 категорически не допускается (снята с поддержки, обновления безопасности не выпускаются)**
- Режим работы php - модуль apache (mod_php)
- время пинга от потенциального пользователя до сервера - менее 150мс
- версия ядра Битрикс 14 и выше

##Общие параметры (рекомендованные)

все что в минимальных, плюс

- версия PHP 5.6 и выше
- версия ядра Битрикс 16 и выше
- доступ к аккаунту хостинга по ssh/sftp
- время пинга от потенциального пользователя до сервера - менее 100мс
- включенный акселератор opcache
- оценка производительности конфигурации по тестированию Битрикс (версии 15) - не ниже 20


##Установки PHP (минимальные)

```ini
safe_mode = Off
short_open_tag = On
realpath_cache_size = 4096k ; и больше
memory_limit = 128M
default_charset = UTF-8
mbstring.func_overload = 2
mbstring.internal_encoding = UTF-8
```

###при использовании opcache

```ini
opcache.validate_timestamps =	1
opcache.revalidate_freq =	0
```

##Установки PHP (рекомендованные)

- доступная память (memory_limit)
  - для визитки, каталога - не менее 128 Mb
  - для магазина - не менее 256 Mb
- позволить загрузку файлов (file_uploads)
- показывать ошибки (display_errors)

##Требуемые модули PHP

- Multibyte String (mbstring)
- MySQL (mysql/mysqli)
- поддержка регулярных выражений (Perl-Compatible)


##Рекомендуемые модули PHP

- MCrypt
- Zlib Compression
- Библиотека GD (функции для работы с графикой)
- Free Type Library

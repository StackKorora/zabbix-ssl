## Проверка даты регистрации доменных имен и действительности SSL сертификатов
Стандартный шаблон предполагает создание узла сети на каждое проверяемое имя, что неудобно и избыточно, так как несколько имен может быть привязано к одному ip адресу.
Реализована концепция сбора всех наблюдаемых имен в один узел. Для обнаружения используется LLD.

Список имен забирается из json файла.

Из этого же списка выделяются доменные имена при помощи предобработки.

Необходимо положить все файлы `externalscripts/*` в каталог внешних скриптов Zabbix, файлы *.sh сделать исполняемыми: `chmod +x zext_ssl_cert.sh list.sh whois_expire.sh`. 
В файл `ssl_check.json` внести данные для мониторинга по аналогии с примером. 


# zabbix-openvpn
Для Zabbix 3.0
Скрипт мониторинга пользователей OpenVPN.
Проверяется статус каждого пользователя OpenVPN, и его входящий\исходящий трафик.

С помощью LLD создаются "узлы сети" по имени файлов сертификатов.

Установка:
1)	скопировать файл discover_vpn.sh в любую директорию, на сервере с OpenVPN (например, /etc/zabbix/scripts/discover_vpn.sh)
	в этом файле указать путь до папки с сетификатами OpenVPN (строка №3).
	
2)	из файла zabbix_agentd.txt скопировать все строки в конец конфига zabbix агента (по умолчанию, /etc/zabbix/zabbix_agentd.conf)
	возможно потребуется изменить путь до discover_vpn.sh
	
3)	импортировать в zabbix шаблон openvpn.xml

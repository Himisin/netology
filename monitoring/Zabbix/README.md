
### Задание 1 

![zabbix](https://github.com/Himisin/netology/blob/main/monitoring/Zabbix/img/Screenshot_244.jpg)

```
sudo apt -y install postgresql

wget https://repo.zabbix.com/zabbix/6.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_6.0-4+ubuntu22.04_all.deb

dpkg -i zabbix-release_6.0-4+ubuntu22.04_all.deb

apt update

apt install zabbix-server-pgsql zabbix-frontend-php php8.1-pgsql zabbix-apache-conf zabbix-sql-scripts zabbix-agent

sudo -u postgres createuser --pwprompt zabbix

sudo -u postgres createdb -O zabbix zabbix

zcat /usr/share/zabbix-sql-scripts/postgresql/server.sql.gz | sudo -u zabbix psql zabbix

sudo nano /etc/zabbix/zabbix_server.conf

systemctl restart zabbix-server zabbix-agent apache2

systemctl enable zabbix-server zabbix-agent apache2

```
---

### Задание 2 


![zabbix2](https://github.com/Himisin/netology/blob/main/monitoring/Zabbix/img/Screenshot_246.jpg)
![zabbix3](https://github.com/Himisin/netology/blob/main/monitoring/Zabbix/img/Screenshot_247.jpg)
![zabbix4](https://github.com/Himisin/netology/blob/main/monitoring/Zabbix/img/Screenshot_248.jpg)



---
## Задание 3 со звёздочкой*
Установите Zabbix Agent на Windows (компьютер) и подключите его к серверу Zabbix.

#### Требования к результаты 
1. Приложите в файл README.md скриншот раздела Latest Data, где видно свободное место на диске C:
--- 

## Критерии оценки

1. Выполнено минимум 2 обязательных задания
2. Прикреплены требуемые скриншоты и тексты 
3. Задание оформлено в шаблоне с решением и опубликовано на GitHub



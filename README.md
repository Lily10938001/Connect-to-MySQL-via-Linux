# Connect-to-MySQL-via-Linux
Practicing for Linux and knowing how to connect it to MySQL. During this period, we can also learn how to interprete php via Linux.

------------------------------------
VirtualBox setting : 
1.	CPU : 3顆
2.	記憶體 : 2000MB 
3.	光碟機 : CentOS 7.9.2009

CentOS : 
1.	localhost login : root
2.	打 ”nmcli” 得到inet4 : IP位址
3.	叫出cmd
4.	輸入”ssh root@IP位址” → “yes” → 輸入password → 即可從本機連線至CentOS的root使用者

連結至網頁前置作業 : 
1.	安裝 HTTP Server : yum install httpd
2.	啟動 HTTP Server : systemctl start httpd
3.	關閉Linux防火牆 : systemctl stop firewalld
4.	暫時關閉Linux安全管理模式 : setenforce 0

要解讀php語言 : yum install php

連結至資料庫
1.	安裝CentOS預設資料庫MariaDB（MySQL）: yum install mariadb-server
2.	啟動MariaDB : systemctl start mariadb
3.	設定MariaDB : mysql_secure_installation
4.	cd到HTML的位置 : cd /var/www/html/
5.	下載資料庫管理系統Adminer : wget https://github.com/vrana/adminer/releases/download/v4.8.1/adminer-4.8.1.php 
6.	ls找到檔名
7.	systemctl restart httpd
8.	在瀏覽器上查詢 ”IP位址/adminer-4.8.1” 
9.	登入後發現仍需下載一些模組 : yum install php-mysqli mysql pdo_ mysql
10.	記得要重新啟動網頁 : systemctl restart httpd  即可成功進入

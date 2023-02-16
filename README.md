# HttpMax

**HttpMax** is a simple, asynchronous, fast and beautiful HTTP library.

```python
import HttpMax
import asyncio

async def main():
    r = await HttpMax.get('https://httpbin.org/basic-auth/user/pass', auth=('user', 'pass'))
    print(r.status_code)
    print(r.headers['content-type'])
    print(r.encoding)
    print(r.text)
    print(await r.json())

asyncio.run(main())
```

HttpMax allows you to send HTTP/1.1 requests extremely easily. There’s no need to manually add query strings to your URLs, or to form-encode your `PUT` & `POST` data — but nowadays, just use the `json` method!

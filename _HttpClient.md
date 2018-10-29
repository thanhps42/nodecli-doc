# _HttpClient

## Constructor
```var c = _HttpClient();```

## Return Object

### ResponseObject
```
{
  "error": string/null,
  "bytes": []bytes,
  "text": string,
  "status": string,
  "statusCode": int,
  "header": []object,
  "cookies": []object
}
```

## Methods

### cookies(url: string): []Cookie
Trả về mảng các cookie thuộc url.

### setProxy(url: string): {error: string/null}
* Thiết lập proxy cho object _HttpClient. Hỗ trợ http, https, socks5, ssh.
* URL theo định dạng: [scheme:][//[username:password@]host]
* Ví dụ: ```http://127.0.0.1:9951```

### closeProxy(): void
Khi setProxy thì phải closeProxy để không bị memory leak.

### followRedirect(bool?): bool
Get/Set redirect

### userAgent(string?): string
Get/Set User-Agent header

### saveCookie(bool?): bool
Get/Set việc _HttpClient có save cookies hay không.

### sendCookie(bool?): bool
Get/Set việc _HttpClient có send cookie đi hay không.

### addParam(string, string): void
Thêm param cho function post.

### addHeader(string, string): void
Thêm header cho lần request tiếp theo.

### get(url: string): [RespnoseObject](###ResponseObject)
* Thực hiện phương thức GET.

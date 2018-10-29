# _HttpClient

## Constructor
```var c = _HttpClient();```

## Methods

### cookies(url: string)
Trả về mảng các cookie thuộc url.

### setProxy(url: string): ErrorObject
* Thiết lập proxy cho object _HttpClient. Hỗ trợ http, https, socks5, ssh.
* URL theo định dạng: [scheme:][//[username:password@]host]
* Ví dụ: ```http://127.0.0.1:9951```

### closeProxy(): void

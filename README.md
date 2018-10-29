# nodecli documentation

# Variables
## $ThreadID: string
Trả về thread ID.

# Methods

## _Sleep(n: int): void
Dừng chương trình trong n milliseconds.

## _Get(name: string): any
Trả về 1 biến global theo name.

## _Set(name: string, value: any): void
Set biến global.

# Command line

## Usage
```nodecli [-threads=1] [-init=<setup.js>] file.js```

## -threads: int
Chạy ```file.js``` bằng ```threads``` luồng.

## -init: string
* Trước khi chạy ```file.js``` đa luồng thì nodecli sẽ chạy file ```<setup.js>``` bằng luồng chính trước.
* Các giá trị global mà ```setup.js``` tạo ra thì ```setup.js``` có thể sử dụng được.
* Nếu không truyền file vào ```-init``` thì nodecli sẽ bỏ qua bươc này mà chạy đa luồng ```file.js```.


# Notes:
* Khi trong thread con nếu muốn sử dụng biến global tạo bởi ```setup.js``` thì nên sử dụng phương thức ```_Get/_Set``` để tránh việc xung đột thread dẫn tốn mất mát dữ liệu.
* Nếu có nhiều lệnh muốn đồng bộ thì xài ```_Lock```.

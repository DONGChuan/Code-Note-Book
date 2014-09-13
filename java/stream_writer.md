# 字节流与字符流

* 字节流继承于InputStream OutputStream
* 字符流继承于InputStreamReader OutputStreamWriter

字符流使用了缓冲区 (buffer),而字节流没有使用缓冲区

底层设备永远只接受字节数据

字符是字节通过不同的编码的包装

字符向字节转换时，要注意编码的问题


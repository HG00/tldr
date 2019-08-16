# curl

> 向/从一个服务器传输数据.
> 支持大多数协议, 包括 HTTP, FTP, 和 POP3.
> 更多信息: <https://curl.haxx.se>.

- 将指定URL的内容下载到文件:

`curl {{http://example.com}} -o {{文件名}}`

- 将文件从URL保存到由URL指示的文件名中:

`curl -O {{http://example.com/文件名}}`

- 下载文件, 跟随 [L]重定向, 并且自动 [C]续传(恢复)前序文件传输:

`curl -O -L -C - {{http://example.com/文件名}}`

- Send form-encoded data (POST request of type `application/x-www-form-urlencoded`):

`curl -d {{'name=bob'}} {{http://example.com/form}}`

- 发送带有额外请求头, 使用自定义请求方法的请求:

`curl -H {{'X-My-Header: 123'}} -X {{PUT}} {{http://example.com}}`

- 发送 JSON 格式的数据, 并附加正确的 `Content-Type` 请求头:

`curl -d {{'{"name":"bob"}'}} -H {{'Content-Type: application/json'}} {{http://example.com/users/1234}}`

- 为服务器授权传入用户名和密码:

`curl -u myusername:mypassword {{http://example.com}}`

- Pass client certificate and key for a resource, skipping certificate validation:

`curl --cert {{client.pem}} --key {{key.pem}} --insecure {{https://example.com}}`
# dirfuzz
多线程网站目录穷举扫描
> 原作者邮箱：ringzero@0x557.org<br />
> 修改完善：NoTrackMe@163.com<br />


# 使用方法
``` shell
python dirfuzz.py www.wooyun.org php
python dirfuzz.py www.wooyun.org asp
python dirfuzz.py www.wooyun.org jsp
```

# 配置说明
``` python
using_dic = './dics/directory-list-2.3-big.txt' # 使用的字典文件
threads_count = 50 # 线程数
timeout = 3 # 超时时间
allow_redirects = True # 是否允许URL重定向
headers = { # HTTP 头设置
	'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_7_3) AppleWebKit/535.20 (KHTML, like Gecko) Chrome/19.0.1036.7 Safari/535.20',
	'Referer' : 'http://www.google.com',
	'Cookie': 'whoami=wyscan_dirfuzz',
}
proxies = { # 代理配置
	# "http": "http://user:pass@10.10.1.10:3128/",
	# "https": "http://10.10.1.10:1080",
	# "http": "http://127.0.0.1:8118", # TOR 洋葱路由器
}
```
# 更新说明
1、去掉无效的刷屏输出，只输出有效信息。
2、动态显示扫描进度

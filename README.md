# cheatsheet

## Beautiful Soup

* 无设限的抓取：
1.import requests
2.resp=requests.get("https://www.douban.com/people/62513788/status/2017535708/")
3.html_str=resp.text
4.from bs4 import BeautifulSoup
5.document=BeautifulSoup(html_str,"html.parser")
6.document

* 设限抓取-加header：
1.import requests
2.import urllib.request
3.url = "http://www.xiami.com/search/song-lyric/page/1?spm=a1z1s.3521881.0.0.&key=%E6%9E%97%E5%A4%95"  
4.req = urllib.request.Request(url)  
5.req.add_header('User-Agent','Mozilla/5.0 (Windows NT 6.1) AppleWebKit/537.36 (KHTML, like   Gecko) Chrome/28.0.1500.72 Safari/537.36')
6.resp = urllib.request.urlopen(req)
7.mainpage = resp.read()
8.document=BeautifulSoup(mainpage,"html.parser")
9.document


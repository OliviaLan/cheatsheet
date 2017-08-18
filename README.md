# cheatsheet

## Beautiful Soup

*import requests
*resp=requests.get("https://www.douban.com/people/62513788/status/2017535708/")
*html_str=resp.text
*from bs4 import BeautifulSoup
*document=BeautifulSoup(html_str,"html.parser")
*document


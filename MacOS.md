## [terminal走代理](https://www.hangge.com/blog/cache/detail_3138.html)

1. 修改配置文件。```vi ~/.zshrc```
2. add config: ```alias proxy='export all_proxy=socks5://127.0.0.1:7890'``` ```alias unproxy='unset all_proxy'```
3. make config affect ```source ~/.zshrc``` 
4. 查询ip地址：```curl ipinfo.io```
5. 启用代理再查询ip地址：```proxy```+```curl ipinfo.io```

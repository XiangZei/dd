[TOC]

### 1. 后台运行服务关闭服务
- nohup  java -jar crm-V5.jar --spring.profiles.active=prod --server.port=80 &
- kill $(ps aux | grep 'java' | grep -v grep | awk '{print $2}')
- .PHONY :special target 避免和同名文件冲突

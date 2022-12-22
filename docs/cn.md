<div align="center">
  <img src="/static/icons/Hotaru.png" width=30%>
</div>

<br>

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10.7-orange">
  <img src="https://img.shields.io/badge/Flask-2.2.2-black">
</div>

<div align="center">
  <a href="/docs/cn.md">中文</a> | <a href="README.md">ENG</a>
</div>

# Hotaru

<details>
  <summary>目录</summary>
  
- [Hotaru](#hotaru)
      - [](#)
  - [简介](#简介)
    - [教程](#教程)
  - [设计](#设计)
</details>

***视频DEMO（英文版）：[点我！](https://youtu.be/PMQW3F9mgek)***

## 简介

Hotaru是一个基于Flask框架和SQLite的在线~~即时通讯~~社交平台。
> **Hotaru还未使用Socket.IO来实现即时通讯。**

这是CS50课程的最终作业项目。

## 教程

1. 配置邮箱：
   ``` Python
   # app.py
   # 该邮箱地址用于给用户发送邮件
   # 例如发送验证链接
   app.config['MAIL_SERVER'] = ''
   app.config['MAIL_PORT'] = ''
   app.config['MAIL_USERNAME'] = ''
   app.config['MAIL_PASSWORD'] = ''
   app.config['MAIL_USE_TLS'] = ''
   app.config['MAIL_USE_SSL'] = ''
   mail = Mail(app)

   # 该邮箱地址用于接收来自用户的报告
   # 例如BUG报告、建议等
   MyEmailAddress = ''
   ```
2. 运行该项目：`python app.py`

## 项目构造

<details>
  <summary>详情</summary>

1. `static`目录包含了：
   - `Hotaru.ico`，网站的头像
   - `scripts.js`
   - `styles.css`
   - `icons`目录
     - 包含了默认用户头像`Hotaru.png`，以及所有被用户上传的自定义头像
2. `templates`目录包含了所有HTML文件
3. `app.py`，项目的主入口
4. `config.py`包含了提供给`app.py`的方法
5. `hotaru.db`是该项目的数据库
   - 包含了用户信息、聊天记录、频道
</details>

## TODO

- [ ] 即时通讯功能
- [ ] 更改用户名或账户密码
- [ ] 私聊
- [ ] 更改文本样式和颜色
- [ ] 发送图片
<div align="center">
<br/>
<br/>
  <h1 align="center">
    Pear Admin Flask
  </h1>
  <h4 align="center">
    開 箱 即 用 的 Flask 快 速 開 發 平 台
  </h4>

  [預覽](http://flask.pearadmin.com:8000)   |   [官網](http://www.pearadmin.com/)   |   [群聊](docs/assets/qqgroup.jpg)   |   [文檔](docs/detail.md)

<p align="center">
    <a href="#">
        <img src="https://img.shields.io/badge/pear%20admin%20flask-1.0.0-green" alt="Pear Admin Layui Version">
    </a>
    <a href="#">
        <img src="https://img.shields.io/badge/Python-3.6+-green.svg" alt="Python Version">
    </a>
      <a href="#">
        <img src="https://img.shields.io/badge/Mysql-5.3.2+-green.svg" alt="Mysql Version">
    </a>
</p>
</div>

<div align="center">
  <img  width="92%" style="border-radius:10px;margin-top:20px;margin-bottom:20px;box-shadow: 2px 0 6px gray;" src="https://images.gitee.com/uploads/images/2020/1019/104805_042b888c_4835367.png" />
</div>

## 項目簡介

Pear Admin Flask 基於 Flask 的後台管理系統，擁抱應用廣泛的python語言，通過使用本系統，即可快速構建你的功能業務
專案旨在為 python 開發者提供一個後台管理系統的範本，可以快速構建資訊管理系統。
專案使用flask-sqlalchemy + 權限驗證 + Flask-APScheduler 定時任務 + marshmallow 序列化與數據驗證

## 内置功能

- [x] 使用者管理：使用者是系統操作者，該功能主要完成系統使用者配置。
- [x] 許可權管理：配置系統功能表，操作許可權，按鈕許可權標識等。
- [x] 角色管理：角色功能表許可權分配。
- [x] 操作日誌：系統正常操作日誌記錄和查詢; 系統異常資訊日誌記錄和查詢。
- [x] 登錄日誌：系統登錄記錄查詢包含登錄異常。
- [x] 服務監控：監視當前系統CPU、記憶體、磁碟、python版本，運行時長等相關信息。
- [x] 檔案上傳： 圖片上傳示例
- [x] 定時任務： 簡單的定時任務

## 項目介紹
項目分為前端與後端兩個部分
### 前端項目
#### layui
layui 是一個前端 JavaScript 框架，使用的底層技術為 es5、jquery。 編寫了一整套 css 樣式、眾多好用的官方元件，使用的類似 amd 的打包方式。 雖說這種技術在現在看來已經過時了，但是對於不想學習太多的前端技術又想做出比較好看的後端程式師、零基礎的新手來說，可以說是上天的恩賜，尤其是在這個前端瘋狂內卷的時代。

layui 框架的上手難度低，同時有完善的官方文檔，對於那些希望快速入門並製作出精美網頁，同時又不想花費太多時間學習前端技術的人來說，layui 是一個非常理想的選擇。

### 前端項目
#### flask
Flask 是一個流行的 Python Web 框架，用於構建 Web 應用程式。 它以其簡單性、靈活性和易用性而聞名。 Flask 遵循 WSGI（Web伺服器閘道介面）規範，旨在輕巧和模組化，使開發人員能夠快速高效地創建 Web 應用程式。

Flask 應用程式提供了堅實的基礎，其簡單性、靈活性和活躍的社區，無論您要開發一個簡單的網站還是一個更複雜的 Web 專案， Flask 都是非常理想的選擇。

## 應用結構

```應用結構
Pear Admin Flask
├─ applications         # 應用
│  ├─ configs           # 配置檔
│  │  ├─ common.py      # 普通配置
│  │  └─ config.py      # 配置文件物件
│  ├─ extensions        # 註冊外掛程式
│  ├─ models            # 數據模型
│  ├─ static            # 靜態資源檔
│  ├─ templates         # 靜態範本檔
│  └─ views             # 視圖部分
│  ├─ admin             # 後台管理視圖模組
│  └─ index             # 前台視圖模組
├─ docs                 # 文檔說明
├─ migrations           # 遷移文件記錄
├─ requirement          # 依賴檔
└─ .env                 # 專案的配置檔
```

## 資源結構

```資源結構
Pear Admin Flask
├─ static           # 項目設定的 Flask 資源資料夾
│  ├─ admin         # pear admin flask 的後端資源檔（與 pear admin layui 同步）
│  ├─ index         # pear admin flask 的前端資源檔
│  └─ upload        # 使用者上傳保存目錄
└─ templates        # 項目設定的 Flask 範本資料夾
  ├─ admin          # pear admin flask 的後端管理頁面範本
  │  ├─ admin_log   # 日誌頁面
  │  ├─ common      # 基本範本頁面（頭部範本與頁腳範本）
  │  ├─ console     # 系統監控頁面範本
  │  ├─ dept        # 部門管理頁面範本
  │  ├─ dict        # 數據自動頁面範本
  │  ├─ mail        # 郵件管理頁面範本
  ├─ photo          # 圖片上傳頁面範本
  ├─ power          # 許可權（功能表）管理頁面範本
  │  ├─ role        # 角色管理頁面範本
  │  ├─ task        # 任務設置頁面範本
  │  └─ user        # 使用者管理頁面範本
  ├─ errors         # 錯誤頁面範本
  └─ index          # 主頁範本
```

## 項目安裝

```bash
# 下載專案
git clone https://gitee.com/pear-admin/pear-admin-flask

# 進入到項目目錄
cd pear-admin-flask

# Venv 虛擬環境安装
python -m venv venv

# 進入到虛擬環境
venv\Scripts\activate.bat

# 安裝依賴
pip install -r requirements.txt
```

## 修改配置

```python
# MySql配置信息
MYSQL_HOST=127.0.0.1
MYSQL_PORT=3306
MYSQL_DATABASE=PearAdminFlask
MYSQL_USERNAME=root
MYSQL_PASSWORD=root

# Redis 配置
REDIS_HOST=127.0.0.1
REDIS_PORT=6379

# 密鑰配置
SECRET_KEY='pear-admin-flask'

# 信箱配置
MAIL_SERVER='smtp.gmail.com'
MAIL_USERNAME='123@gmail.com'
MAIL_PASSWORD='XXXXX' # 應用程式密碼
```

## 運行項目

```bash
# 初 始 化 數 據 庫
flask db init
flask db migrate
flask db upgrade
flask admin init
```

執行 python app.py 命令啟動項目

## 命令行創建視圖

```bash
# 示例

flask new --type view --name test/a

# 自動註冊藍圖
# 訪問http://127.0.0.1:5000/test/a/
```

## 使用docker-compose運行项目

```bash
git clone https://gitee.com/pear-admin/pear-admin-flask

#安装docker-compose 
curl -L https://github.com/docker/compose/releases/download/1.26.2/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose 

#運行如下命令，有輸入版本，表示docker-compose 可以用了
docker-compose --version 

#在當前目录執行如下命令即可以運行app
docker-compose -f dockercompose.yaml up

#看到如下表示運行成功，由於pip下載慢，需要一些時間，請耐心等待；如果安装失敗，重新執行上面的命令即可。

#運行後再瀏覽器訪問127.0.0.1：5000 

#如果要停止容器運行，在當前文件夹執行如下命令：
docker-compose -f dockercompose.yaml dwon


```

## 預覽项目

|                        |                        |
| ---------------------- | ---------------------- |
| ![](docs/assets/1.jpg) | ![](docs/assets/2.jpg) |
| ![](docs/assets/3.jpg) | ![](docs/assets/4.jpg) |
| ![](docs/assets/5.jpg) | ![](docs/assets/6.jpg) |

## 相關教學影片
### 推薦觀看順序

#### (一)
[Python免费开源的后端管理系统：pear admin flask 介绍及运行教程](https://www.bilibili.com/video/BV1JF411L73c/)

#### (二)
[Python后端管理系统：pear admin flask 二次开发](https://www.bilibili.com/video/BV1fA4y1o7SL/)


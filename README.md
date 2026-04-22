# 个人主页网站

一个现代化的个人主页网站，使用Flask框架构建，具有响应式设计和美观的界面。

## 功能特点

- 🎨 现代化的响应式设计
- 📱 移动端友好
- 🚀 基于Flask框架
- 💡 流畅的动画效果
- 🔗 社交媒体集成
- 📧 联系表单
- 🎯 项目展示

## 项目结构

```
personalweb/
├── app.py                 # Flask应用主文件
├── requirements.txt       # Python依赖
├── templates/            # HTML模板
│   ├── base.html        # 基础模板
│   ├── index.html       # 首页
│   ├── about.html       # 关于页面
│   ├── projects.html    # 项目页面
│   └── contact.html     # 联系页面
└── static/              # 静态资源
    ├── css/
    │   └── style.css    # 样式文件
    └── js/
        └── script.js    # JavaScript文件
```

## 安装步骤

1. 克隆项目到本地：
```bash
git clone https://github.com/dorrris01/personalweb.git
cd personalweb
```

2. 创建虚拟环境（推荐）：
```bash
python -m venv venv
```

3. 激活虚拟环境：
- Windows:
```bash
venv\Scripts\activate
```
- macOS/Linux:
```bash
source venv/bin/activate
```

4. 安装依赖：
```bash
pip install -r requirements.txt
```

## 运行项目

1. 启动Flask应用：
```bash
python app.py
```

2. 在浏览器中访问：
```
http://localhost:5000
```

## 页面说明

### 首页
- 个人介绍
- 技能展示
- 最新项目预览

### 关于我
- 个人经历
- 技术栈展示
- 时间线展示

### 项目
- 项目展示
- 技术标签
- 项目链接

### 联系我
- 联系方式
- 社交媒体链接
- 联系表单

## 自定义配置

### 修改个人信息
在相应的HTML模板中修改个人信息，如：
- 姓名
- 联系方式
- 社交媒体链接
- 项目信息

### 修改样式
编辑 `static/css/style.css` 文件来自定义网站样式。

### 修改颜色主题
在 `style.css` 文件中修改CSS变量：
```css
:root {
    --primary-color: #3498db;
    --secondary-color: #2ecc71;
    --dark-color: #2c3e50;
    --light-color: #ecf0f1;
}
```

## 部署

### 使用Gunicorn部署

1. 安装Gunicorn：
```bash
pip install gunicorn
```

2. 运行应用：
```bash
gunicorn -w 4 -b 0.0.0.0:5000 app:app
```

### 使用Docker部署

创建 `Dockerfile`：
```dockerfile
FROM python:3.9-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 5000

CMD ["gunicorn", "-w", "4", "-b", "0.0.0.0:5000", "app:app"]
```

构建和运行：
```bash
docker build -t personalweb .
docker run -p 5000:5000 personalweb
```

## 技术栈

- **后端**: Flask (Python)
- **前端**: HTML5, CSS3, JavaScript
- **样式**: 自定义CSS
- **图标**: Font Awesome
- **开发工具**: Git, VS Code

## 贡献

欢迎提交问题和拉取请求！

## 许可证

MIT License

## 联系方式

- GitHub: [@dorrris01](https://github.com/dorrris01)
- 邮箱: your.email@example.com

## 更新日志

### v1.0.0 (2026-03-14)
- 初始版本发布
- 基础页面结构
- 响应式设计
- 动画效果

---

享受使用这个个人主页网站！如有任何问题，请随时联系我。
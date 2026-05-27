<center><h1> GitHub 仓库卡片组件</h1></center>

> 一款在网页上展示GitHub仓库的轻量级组件

English | [简体中文](/readme-zh.md)

## 特性
- 从GitHub自动拉取仓库信息.

- 响应式布局.

- 无依赖，仅需两行代码就能展示仓库卡片.

# 食用方法
1. 引入JS文件
```html
<script src="github-card.js"></script>
```
2. 以以下形式添加一个div，`data-github-repo`字段包含用户名和仓库
```html
<div data-github-repo="owner/repo"></div>
```
3. (可选) 当有多个卡片一起摆放时，可以嵌套一个github-cards-grid类的div获得响应式布局
```html
<div class="github-cards-grid">
  <div data-github-repo="link9596/Github-Card"></div>
  <div data-github-repo="vuejs/vue"></div>
</div>
```

4. (可选) GitHub默认的Api请求有速率限制（每小时60次，对于个人网页展示等已经足够），但你还可以添加Access Token来提高限制（每小时5000次）
在载入JS之前加上:

```html
<script>
  window.GithubCardToken = 'your_personal_access_token';
</script>
<script src="github-card.js"></script>
```


实例
```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>My GitHub projects</title>
</head>
<body>
  <div class="github-cards-grid">
    <div data-github-repo="link9596/Github-Card"></div>
    <div data-github-repo="vuejs/vue"></div>
  </div>
  <script src="github-card.js"></script>
</body>
</html>
```

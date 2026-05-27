# GitHub Card Widget
> A lightweight, zero‑dependency widget that displays GitHub repository stats as a card.

English | [简体中文](/readme-zh.md)

## Features
- Auto‑fetches stars, forks, description, and primary language from GitHub API.

- Responsive grid layout.

- No build step, no external dependencies.

# Usage
1. Include the script
```html
<script src="github-card.js"></script>
```
2. Add a container with the repository name
```html
<div data-github-repo="owner/repo"></div>
```
3. (Optional) Wrap multiple cards in a grid container for responsive grid layout.
```html
<div class="github-cards-grid">
  <div data-github-repo="link9596/Github-Card"></div>
  <div data-github-repo="vuejs/vue"></div>
</div>
```

4. (Optional) Increase API rate limit with a GitHub token
Place this before the script tag:

```html
<script>
  window.GithubCardToken = 'your_personal_access_token';
</script>
<script src="github-card.js"></script>
```
Without a token: 60 requests per hour.
With a token: 5,000 requests per hour.

Example
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

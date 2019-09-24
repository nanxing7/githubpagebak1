---
title: 从0配置一个Hexo
date: 2019-09-24 03:56:14
tags: Hexo
---
## 从0配置一个Hexo



### .travis.yml 配置代码
```yml
sudo: false
language: node_js
node_js:
  - 10 # use nodejs v10 LTS
cache: npm
branches:
  only:
    - hexo # build master branch only
script:
  - npm install hexo-generator-search --save # 安装本地搜索插件
  - npm audit fix # 执行修复命令
  - hexo generate # generate static files
deploy:
  provider: pages
  skip-cleanup: true
  github-token: $GH_TOKEN #这是一个变量，不要动它，这个变量代表着从 github 设置到的 token
  keep-history: true
  on:
    branch: hexo
  local-dir: public
  target_branch: master

```
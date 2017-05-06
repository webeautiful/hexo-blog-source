# hexo-blog-source

### REQUIRES
* nodejs
* git
* hexo
* yarn/npm

### Initialize
```bash
yarn init blog-name
```

### 开发环境搭建
```bash
git clone git@github.com:webeautiful/hexo-blog-source.git
yarn install
yarn add hexo-deployer-git # hexo deploy失败时，安装此插件可解决

```

### 配置
#### CNAME
* `_config.yml`配置, 如: `url: http://www.etuai.com`
* CNAME文件放在`source/`目录下
#### `themes/landscape`
* `_config.yml`配置, 如: `theme: landscape` 

### 添加新文章
```bash
hexo new [layout] <title>
```

### 部署
#### 修改`_config.yml`配置:
```
deploy:
  type: git
  repo: git@github.com:webeautiful/webeautiful.github.io.git
  branch: master
```
#### 部署到Github Page
```bash
hexo clean
hexo g
hexo deploy
```

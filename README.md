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

#### 配置CNAME
* CNAME文件放在`source/`目录下
* `_config.yml`配置, 如: `url: http://www.etuai.com`
#### 配置themes
* 创建`themes`目录
* 安装主题`git clone https://github.com/iissnan/hexo-theme-next.git themes/next`
* 主题目录, 如: `themes/next`
* `_config.yml`配置, 如: `theme: next` 

### 启动开发环境
```bash
$ hexo s --debug
```

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

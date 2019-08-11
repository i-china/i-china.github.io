---
title: Hexo
date: 2019-08-11 10:59:43
tags: Hexo
categories: Hexo
copyright: true
top: 99

---

<center> Hexo 基础和语法 </center>

<!-- More --> 

`npm install -g hexo-cli`  
`hexo init <Folder>`  
`npm install`  
`vim package.json`  
` hexo new [layout] <title> `  
` hexo generate = hexo g `  
` hexo publish [layout] <filename> `   
` hexo server -p xxxx -s --static -l --log `
` hexo deploy = hexo d`  
` hexo render <file1> [file2] ... -o --output `  
` hexo migrate `  
` hexo clean = hexo c `   
` hexo list <type> `  
` hexo version `  
` hexo --safe `   
` hexo --debug `  
` hexo --silent `  
` hexo --config custom.yml`   
` hexo --draft`  
` hexo --cwd /path/to/cwd `

` npm install hexo-migrator-rss --save `
` hexo migrate rss <source> `  
` npm install hexo-migrator-wordpress --save`  
` hexo migrate wordpress <source>`  

### Write
`  hexo new [layout] <title> `  
` layout:  post > source/_posts    page  > source     draft 	> source/_drafts `  
` hexo new photo "TEXT" `  

### Front-Matter
```
title: TEXT
date: DATE
updated: UPDATE_TIME
comments: true
tags: TEXT
categories: TEXT
permalink: url
keywords: TEXT
copyright: true   


Tag Plugins

引用块
{% blockquote [author[, source]] [link] [source_link_title] %} 
content 
{% endblockquote %} 

代码块
{% codeblock [title] [lang:language] [url] [link text] %}
code snippet
{% endcodeblock %} 

    
反引号代码块

{% pullquote [class] %}
content
{% endpullquote %}  
```
   
### SERVER 
`npm install hexo-server --save`
` hexo server -p 5000`
` hexo server -s` 
` hexo server -i 192.168.1.1` 

### MADE FILES
`hexo generate` 
` hexo generate --watch` 
` hexo generate --deploy` 
` hexo deploy --generate` 
` hexo g -d `
` hexo d -g` 

### DEPLOY 
`npm install hexo-deploy-git --save` 
` hexo deploy `
` deploy: 
	type: git
	repo: <repository url>
	branch: [branch_name]
	message: [message]
`

### SFTP
`npm install hexo-deployed0-sftp --save`
`vim _config.yml
deploy:
	type: sftp
	host: <host>
	user: <user>
	pass: <password> 
	remotePath: [remote path]
	port: [port]
	privateKey: [path/to/privateKey]
	passphrase: [passphrase]
	agent: [path/to/agent/socket]
`

### PERMALINKS
`vim _config.yml
permalink_defaults: 
	lang: en|zh-Hans
`

### THEME
`git clone git@github.com/<username>/xxx.git theme/xxx
cd xxx
npm install`

### TEMPLATE
` 
index  		首页
post		文章
page		分页	
archive		归档
category	分类
tag		标签
`

### 具体看官方API
[HEXO-DOC](https://hexo.io/zh-cn/docs/ "HEXO_DOC")













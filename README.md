# getbook

# 功能
该项目主要是用于采集在线小说，按章节将小说下载为.txt文件

# 使用运行方法
  
  1、clone项目
  
  2、npm install
  
  3、node app.js 小说名称

# 提示
  
  1、执行错误的话，请将项目根目录下的config.json中的isInit值改为false（该方法仅在第一次运行出错时使用）

# 实现功能
  
  1、由于采集的网站为每个访问者配置了不同的key。故首次运行时抓取key，并将key保存在本地配置文件中，以便下次使用。
  
  2、搜索小说，名称匹配时直接开始按目录章节下载小说。 匹配时列出相似小说。
  
  3、本地保存已下载小说，下次搜索同名小说时，可直接获取小说目录地址，并跳过已存在的章节。

# config.json说明
  
  1、domain:      网站的地址 （请勿修改）
  
  2、searchId:    网站所需的key (首次运行时自动获取）（请勿修改）
  
  3、searchUrl：  网站的小说搜索页面 （请勿修改）
  
  4、isUseCache： 搜索小说时是判断本地已有的小说，true仅更新新章节， false全部从新下载 （可修改）
  
  5、nextMinite： 抓取每章节内容的时间间隔，单位（秒） (防止被屏蔽）（可修改，建议大于10）
  
  6、isInit：     配置信息是否已经初始化，主要用于判断是获已取到key （修改为false时，下次运行会重新获取key)

#待实现功能
  
  1、一次指下载多本小说
  
  2、整本小说下载完后，将所有.txt文件打包为rar文件



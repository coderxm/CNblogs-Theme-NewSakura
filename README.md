<div align="center">
<img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1597236938438&di=c9a51694bd9cd7e0d18d3cf440e92593&imgtype=0&src=http%3A%2F%2Fgss0.baidu.com%2F9vo3dSag_xI4khGko9WTAnF6hhy%2Fzhidao%2Fpic%2Fitem%2Fa6efce1b9d16fdfacee8dd40b48f8c5495ee7b93.jpg" height="150px" width="150px"/>

[![GitHub release](https://img.shields.io/badge/Release-v1.0.0-green)](https://github.com/coderxm/Cnblogs-Theme-NewSakura/releases)
[![GitHub contributors](https://img.shields.io/badge/contributors-1-green)](https://github.com/coderxm/Cnblogs-Theme-NewSakura/graphs/contributors)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue)](https://github.com/coderxm/Cnblogs-Theme-NewSakura/blob/master/LICENSE)
</div>

# CNblogs-Theme-NewSakura
* 基于Sakura美化方案改造的博客园样式：NewSakura
* 如使用了本样式，请给个Star。

## 项目结构
 ```
                            |--sidebar.html 侧边栏代码
 |--CNblogs-Theme-NewSakura—|--main.css   自定义css代码
 |			    |--main.js    引用js
 |			    |--foot.html  页脚代码
 |--img-|--效果1.jpg
 |	|--效果2.jpg
 |README.md
 ```
 
 有js权限，期间将侧边栏、页脚和css代码粘贴进博客园设置内即可！代码文件内有相应注释，根据它修改即可。
## 功能简介

依次分重点：
* 新增暗黑白昼模式，白天暗黑刺激
* 首页及随笔页头图随机切换
* 音乐播放器，使用Aplayer插件
* 看板娘，原先的主题已失效，现已修改
* 自动生成文章目录，基本功能
* 导航菜单子目录，照葫芦画瓢添加
* 图片灯箱、滚动进度条
* 文章打赏
* 其他网站链接，非必需
* 将首页底部不必要的滚动条去掉
* 修改了文章评论区的框框大小，原先的过大变形
* 暗黑白昼切换不影响评论区，暗黑字白，白昼字黑
* 修改了分类页面样式，为了在暗黑后看的清楚美观

注意：目前Sakura还不支持响应式，所以还需大家帮忙喽！

## 主题预览
![效果1](https://images.cnblogs.com/cnblogs_com/coderma/1826417/t_200812032842%E6%95%88%E6%9E%9C1.JPG)
![效果2](https://images.cnblogs.com/cnblogs_com/coderma/1826417/t_200812032853%E6%95%88%E6%9E%9C2.JPG?a=1597202946068)

## 主题部署

<div class="info"><p>快速搭建出与本博客一样的样式，	请看下面这句说明，当然前提是得有<span style="color: red">js权限</span></p></div>

部署和本博客一样的主题，请直接下载整个主题，对应的改下**文件链接地址** ，把**css**、**侧边栏**、**页脚**代码粘贴的你的博客后台就行。为了个性化定制，如果你想个性化定制博客，请往下看基本部署。

### 基本部署

* 前提：已经开通`js`权限

* 设置皮肤选择自定义custom

* 引入样式
  把**main.css**中的代码粘贴到自定义css中，无需个性化操作

* 引入文件
  放在侧边栏html文件中，本人已为你添加。建议下载该文件并上传博客园，之后只需修改样式引入即可！

  ```javascript
  <script src="https://blog-static.cnblogs.com/files/coderma/main.js"></script>
  ```

* 顶部菜单设置

  将以下链接替换成自己随笔地址，以下代码在`main.js`中,建议打开该文件查看并修改

  ```javascript
  $("#navList").append('<li><a id="blog_nav_myyoulian" class="menu"href="https://www.cnblogs.com/coderma/p/1117239.html">友链</a><i></i></li><li><a id="blog_nav_myzanshang" class="menu" href="https://www.cnblogs.com/coderma/p/1133477.html">赞赏</a><i></i></li><li><a id="blog_nav_myguanyu" class="menu" href="">关于</a></li>');
  ```

* 菜单icon设置
    
   就是菜单前的小图标，感兴趣的可以去了解一下[Font awesome](http://fontawesome.dashgame.com/ )

    ```javascript
            //博客title
			//去掉rss替换成分类
			$('#blog_nav_rss').replaceWith('<a id="blog_nav_fenlei" class="menu" href="https://www.cnblogs.com/coderma/p/13458241.html" target="_self">分类</a>');  //可替换以下链接
			$("#navList").append('<li><a id="blog_nav_myyoulian" class="menu" href="https://www.cnblogs.com/coderma/p/13413494.html" target="_self">友链</a><i></i></li><li><a id="blog_nav_myarchive" class="menu" href="https://www.cnblogs.com/coderma/p/13414527.html" target="_self">归档</a><i></i></li><li><a id="blog_nav_myguanyu" class="menu" >关于</a></li>');
			//添加标签图标
			$('#blog_nav_sitehome').prepend('<i class="fa fa-fort-awesome" aria-hidden="true"></i>');   //博客园
			$('#blog_nav_myhome').prepend('<i class="fa fa-home" aria-hidden="true"></i>');				//首页
			$('#blog_nav_newpost').prepend('<i class="fa fa-edit" aria-hidden="true"></i>');			//新随笔
			$('#blog_nav_contact').prepend('<i class="fa fa-address-book-o" aria-hidden="true"></i>');	//联系
			$('#blog_nav_fenlei').prepend('<i class="fa fa-filter" aria-hidden="true"></i>');			//分类
			$('#blog_nav_admin').prepend('<i class="fa fa-cog" aria-hidden="true"></i>');				//管理
			$('#blog_nav_myyoulian').prepend('<i class="fa fa-link" aria-hidden="true"></i>');			//友链
			$('#blog_nav_myarchive').prepend('<i class="fa fa-archive" aria-hidden="true"></i>');		//赞赏
			$('#blog_nav_myguanyu').prepend('<i class="fa fa-universal-access" aria-hidden="true"></i>');//关于
			//添加li内嵌ui
			
    ```

*  菜单子目录设置

     菜单子目录，在**关于**菜单下添加了子目录,相应的样式可自行修改添加!

    ```javascript
    let guanyu = '<ul class="sub-menu">' +
		'<li><a href=" " target="_self"><i class="fa fa-user-o" aria-hidden="true"></i>博主</a></li>' +   //添加关于文章链接
		'<li><a id="blog_nav_theme" onclick="changeTheme();" ><i class="iconfont icon-taohua" aria-hidden="true"></i> 主题</a></li>' +  //主题/暗黑白昼模式
		'</ul>';
		$('#blog_nav_myguanyu').after(guanyu);
    ```

* 脚本设置

  为了配置方便，我在侧边栏里设置了一些常用参数，可根据下表选择需要开启和配置

  ```javascript
  <script type="text/javascript"> 
	$.silence({
        profile: {
            enable: true,
            avatar: 'https://images.cnblogs.com/cnblogs_com/coderma/1820127/o_200803093536logo.png', //头像，可修改
            favicon: '',
            notice: '个人博客地址：https://index.maliaoblog.cn/  欢迎大家来踩'   //通知，可修改
        },
        catalog: {
            enable: true,
            move: true,
            index: true,
            level1: 'h2',
            level2: 'h3',
            level3: 'h4',
        },
        signature: {
            enable: true,
            home: 'https://www.cnblogs.com/coderma/',  //主页链接，可修改
            license: 'CC BY 4.0',
            link: 'https://creativecommons.org/licenses/by/4.0'
        },
        sponsor: {
            enable: true,
            paypal: null,
            wechat: '',  //赞助，可修改图片链接
            alipay: ''
        },
        github: {
            enable: false,
            color: '#fff',
            fill: '#FF85B8',
            link: 'https://github.com/coderxm'  //可修改
        },
	  topImg: {
		homeTopImg: [
      "https://img2020.cnblogs.com/blog/2027366/202008/2027366-20200807133710823-1221571975.jpg",   //主页顶部图片，可修改
					],
              notHomeTopImg: [
      "https://img2020.cnblogs.com/blog/2027366/202008/2027366-20200807132804040-1889645361.jpg",  //可修改
					]
		},
	  topInfo: {
			title: 'Hi,流浪舟',  //首页标题（可替换）
			text: "No one choose this life for me But I don't mind it",  //首页横幅语句
			github: "https://github.com/coderxm/",      //github(替换成相应链接)
			weibo: "",
			telegram: "",
			music: "",
			twitter: "",
			zhihu: "",
			mail: "",
		}       
    });
  </script>
  ```

  参数说明表：

  | 模块                     | 属性          | 说明             | 类型    | 默认值                                                       |
  | :----------------------- | ------------- | ---------------- | ------- | ------------------------------------------------------------ |
  | profile（基础信息）      | enable        | 是否启用         | Boolean | true                                                         |
  |                          | avatar        | 作者头像         | String  |                                                              |
  |                          | favicon       | 网站标题图标     | String  |															   	 |
  |                          | notice        | 公告             | String  |感谢使用该主题                                                |
  |                          | authorName    | 作者姓名         | String  |coderxm		  												 |
  | catalog（博文目录）      | enable        | 是否启用         | Boolean | false                                                        |
  |                          | move          | 是否允许拖拽     | Boolean | true                                                         |
  |                          | index         | 是否显示索引     | Boolean | true                                                         |
  |                          | level1        | 一级标题         | String  | h2                                                           |
  |                          | level2        | 二级标题         | String  | h3                                                           |
  |                          | level3        | 三级标题         | String  | h4                                                           |
  | signature（博文签名）    | enable        | 是否启用         | Boolean | true                                                         |
  |                          | home          | 作者主页         | String  | [https://www.cnblogs.com](https://www.cnblogs.com/)          |
  |                          | license       | 许可证名称       | String  | CC BY 4.0                                                    |
  |                          | link          | 许可证链接       | String  | <https://creativecommons.org/licenses/by/4.0>                |
  | sponsor（博文赞赏）      | enable        | 是否启用         | Boolean | false                                                        |
  |                          | paypal        | PayPal 收款地址  | String  | null                                                         |
  |                          | alipay        | 支付宝收款二维码 | String  | null                                                         |
  |                          | wechat        | 微信收款二维码   | String  | null                                                         |
  | github（GitHub Corners） | enable        | 是否启用         | Boolean | false                                                        |
  |                          | fill          | 背景填充色       | String  | [Silence Theme Color]                                        |
  |                          | color         | 章鱼猫颜色       | String  | #fff                                                         |
  |                          | link          | Github 链接      | String  | null                                                         |
  | topImg（头图）           | homeTopImg    | 首页头图         | Array   | 					                                         |
  |                          | notHomeTopImg | 文章和随笔页头图 | Array   | 															 |
  | topInfo(首页头图信息)    | titile        | 头部标题         | String  | Hi, 流浪舟!                                                  |
  |                          | text          | 横幅标题         | String  | No one choose this life for me But I don't mind it  		 |
 
配置完成后，记得点击「保存」按钮。 

## 个性化定制

### 新增暗黑白昼模式
开始的时候是暗黑的，在**关于**下的子菜单栏内，点击主题可切换成白昼模式。 

### 菜单新增分类、友链、博主、归档栏
原理简单，只需先新建随笔即可，并替换链接，点击便可跳转到相应页面。关于分类，去掉了过去的RSS，换成博客园已有的分类，同样的方法，将所有分类链接收录到某一随笔中即可，随笔链接即是分类栏链接。博主一栏写你的信息，归档类似，我相信这样的问题难不倒有大智慧的你！

### 首页及文章大图

首页和随笔以及文章页的头图都是随机切换的，添加图片在侧边栏html配置中。这里类型为随笔的时候头部会显示**标题**、**头像**、**作者**、**发布时间**、**阅读数**，而类型为文章的时候只会显示标题，根据情况选择类型发布。
请尽量选择像素1920*1080px的高清大图，这样的话首页图片会更适合。

### 随笔预览图

![预览](https://images.cnblogs.com/cnblogs_com/coderma/1826417/t_200812032853%E6%95%88%E6%9E%9C2.JPG?a=1597202946068)


在写随笔或者文章的时候添加摘要图片和摘要文字，**摘要文字一定要添加**，如果不添加摘要图片会给一张默认图片。

### 回顶部钩子

```javascript
//回到顶部特效
			$('body').prepend(`<a href="#" class="cd-top faa-float animated cd-fade-out" target="_self"></a>`);
			let $win = $(window);
			let oldScrollY = 0;
			$win.scroll(function () {
				oldScrollY = this.scrollY;
				let height = window.innerHeight;
				let top = '-' + (900 - height + 80) + 'px';
				if (oldScrollY > 0) {
					$('.cd-top').css('top', top);
				} else {
					$('.cd-top').css('top', '-900px');
				}
			});
```	
		
### 公告


公告内容修改在侧边栏基础信息配置中，修改`notice`，代码中已有提示

### 看板娘

我个人博客的看板娘是引用别人的，同一个，失效了会及时修复的！将以下代码添加到页脚，当然本人又已经为你添加好了，所以过程非常轻松！

```javascript
  <script src="https://eqcn.ajz.miesnfu.com/wp-content/plugins/wp-3d-pony/live2dw/lib/L2Dwidget.min.js"></script>
  <script src="https://common.cnblogs.com/scripts/jquery-2.2.0.min.js"></script>
```

### 音乐播放器

相信看过我以前文章的同学对这个一定不会陌生，怎么获取id我也不在这里罗嗦了，可以去找我的文章，获取到id之后把下面的id替换掉就可以了！

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/aplayer@1.10.0/dist/APlayer.min.css">
<script src="https://blog-static.cnblogs.com/files/zouwangblog/APlayer.min.js"></script>
<script src="https://unpkg.com/meting@1.2/dist/Meting.min.js"></script>
<div id="player" class="aplayer aplayer-withlist aplayer-fixed" data-id="7660234225" data-server="tencent" data-type="playlist" data-order="random" data-fixed="true" data-listfolded="true" data-theme="orangered"></div>
<!-- end -->
```

### 博客logo

左上角的logo，修改文字需要到`main.js`里找到以下代码，替换文字即可，如果不喜欢可以注掉,我也觉得没啥好看，main.js里我已经删了！

```javascript
   var title = '<div class="site-branding">' +
		'<span class="logolink moe-mashiro">' +
		'<ruby><span class="sakuraso">漂泊</span><span class="no">的</span><span class="shironeko">流浪舟</span>' +
		'<rt class="chinese-font">漂泊的流浪舟</rt></ruby></a></span>' +
		'</div>'
		$('body').prepend(title);
```

### 页面滚动进度条

页面滚动的时候会在顶部出现一个橙色的进度条，修改颜色到页面css里，找到以下代码修改`background`

```css
.scrollCls {
    position: fixed;
    top: 0;
    height: 3px;
    background: orange;
    transiton-property: width,background;
    transition-duration: 1s,1s;
    z-index: 99999;
}
```

### 首页个人信息

* 名称
  在侧边栏配置中修改`topInfo`里的`title`

* 座右铭（横幅标题）
  在侧边栏配置中修改`topInfo`里的`text`

* 其他网站链接(已注释，大都是推特等国外app，影响美观)
  在侧边栏配置中修改`topInfo`里对应的链接地址

## 写在最后

我把这个美化分享了出去，以我目前的前端技术改造这么个样式也很费劲的，毕竟不是专业做前端的！这是我在博客园的一篇美化文章了，博客还是有很多改进的，希望采用这个样式的你能够多多支持，有什么问题都可以提交，我也会及时为大家解决。最后也欢迎大家光临我的小站 https://www.maliaoblog.cn

## 微信公众平台
微信搜索 “菜鸡干Java” 关注，里面有加群，可以一起交流！

## 项目地址

[GitHub地址](https://github.com/coderxm/CNblogs-Theme-NewSakura )

[Gitee地址](https://gitee.com/openkit/CNblogs-Theme-NewSakura )



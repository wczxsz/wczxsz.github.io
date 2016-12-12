## 注意事项
* 更新完文章详情页后，记得要同步更新频道主页和频道更多页。
* 每篇文章详情页的评论是独立的，所以记得要更新每篇文章评论部分的 ID 、标题和文章全链接。

## 网站目录结构
```
/            //根目录，对应域名 wczxsz.com
/index.html  //网站首页
/assets/img/...  //图片目录，图片都要存在这里
/public/...         //对应5个频道目录和页面

//下面是模板文件，可以用于复制创建新页面

/channel.html   //频道模板
/more.html      //频道更多模板
/article.html   //文章详情页模板
```

## 首页维护要求 */index.html*

* 活动照片 */assets/img/home.jpg* 需要深色背景，像素尽量高点，参考 *home.jpg* 。
* 人头像照片和企业logo照片像素为 *400×400*。
* 头像链接到*校友故事* 文章详情页面。

## 频道目录结构

```
/public/service                //校友服务
/public/service/index.html     //频道首页
/public/service/more.html      //频道更多页面
/public/service/article.html   //频道文章详情页模板，用于复制代码生成详情页

```

## 文章详情页维护要求 *article.html*
* 修改文章标题、作者和日期
```
<section class="wz-article">
  <div class="container">
    <!-- 1、替换掉标题文字 -->
    <h2>深圳文昌中学校友会简介</h2>
    <div class="lead">
      <!-- 2、替换掉作者 -->
      <span class="author">韩和喜</span>
      <!-- 3、替换掉日期-->
      <span class="date">2016-11-11</span>
    </div>
    ...
```
* 添加视频
```
<!-- 1、先把视频上传至视频网站，比如优酷 -->
<!-- 2、在适当位置添加如下从视频网站拷贝的代码 -->
<!-- 3、多个视频，依次添加 -->
 <iframe height=498 width=501 src='http://player.youku.com/embed/XMTgzMjM5NzM2OA==' frameborder=0 'allowfullscreen'></iframe>

```
* 添加照片
```
<!-- 1、添加如下代码块到适当位置，并修改*img*标签 *src*值 -->
<!-- 2、多张照片可重复复制多份代码块，并修改照片路径 -->
<!--添加照片 start-->
<div class="row">
  <div class="col-xs-12 col-sm-12 col-md-12">
    <!-- 修改src值为照片路径 -->
    <img src="/assets/img/home.jpg" alt="" />
  </div>
</div>
<!--添加照片 end-->

```
* 添加小标题和文章段落
```
<!--1、小标题放在 h3 标签里，需要的话，替换掉内容，可以随意增加，注意包括标签内容一起拷贝 -->
<h3>业务范围</h3>
<!--2、每个段落放在 p 标签里，需要的话，替换掉内容，可以随意增加，注意包括标签内容一起拷贝 -->
<p>文昌中学深圳校友会的业务范围包括：</p>
<p>(一) 加强校友间、校友和母校的联系和情况交流；</p>
<p>(二) 促进校友为国家建设和母校的发展作贡献；</p>
<p>(三) 进行学术交流；</p>
<p>(四) 组织联谊活动；</p>
<p>(五) 编辑、印刷《校友通讯》等内部刊物。</p>
```
* 添加文章评论
...

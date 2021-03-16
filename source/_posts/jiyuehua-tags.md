---
title: 集约化平台标签
date: 2021-03-15 11:29:33
categories: 
- 集约化平台
toc: true
cover: /gallery/covers/vector_landscape_1.svg
thumbnail: /gallery/covers/vector_landscape_1.svg
---

本篇文章总结了开普集约化平台的常用标签。

<!-- more -->

# 栏目
```html
<CMSPRO_WEBSITE FIELD='url'></CMSPRO_WEBSITE>
<CMSPRO_CHANNEL CODE='' FIELD='url'></CMSPRO_CHANNEL>
<CMSPRO_CHANNEL CODE="" FIELD="channelName"></CMSPRO_CHANNEL>
<CMSPRO_CHANNEL CODE="" FIELD="memo">栏目描述</CMSPRO_CHANNEL>
```

# 获取文章
```html
<CMSPRO_DOCUMENTS CHANNELCODE="" DOCUMENTTYPE="0|1|2|3|8|9" NUM="5" STARTPOS="0"></CMSPRO_DOCUMENTS>
<CMSPRO_DOCUMENTS CHANNELCODE="" DOCUMENTTYPE="0|1|2|3|8|9" NUM="1000" STARTPOS="0" PAGENAVIGATIONID="page-div" PAGENAVIGATIONCLASS="" PAGESIZE="0"></CMSPRO_DOCUMENTS>
（SITECODE='chengdu' 跨站点读取数据）
（ORDER="PUBLISHED_TIME DESC" 文章列表排序字段）
<CMSPRO_APPENDIXS MODE="IMG" NUM="1" STARTPOS="0"></CMSPRO_APPENDIXS>
<CMSPRO_APPENDIX FIELD='path'></CMSPRO_APPENDIX>
<CMSPRO_DOCUMENT FIELD='url'></CMSPRO_DOCUMENT>
<CMSPRO_DOCUMENT FIELD="title">文章标题</CMSPRO_DOCUMENT>
<CMSPRO_DOCUMENT FIELD="content">文章内容</CMSPRO_DOCUMENT>
<CMSPRO_DOCUMENT FIELD="publishedTime" DATEFORMAT="yyyy-MM-dd">时间</CMSPRO_DOCUMENT>
```

# 获取子栏目
```html
<CMSPRO_CHANNELS CODE="" CHILDLEVEL="1" CHILDTYPE="0|1|2|3" NUM="" STARTPOS="0"></CMSPRO_CHANNELS>
<CMSPRO_CHANNEL FIELD='url'></CMSPRO_CHANNEL>
<CMSPRO_CHANNEL FIELD="channelName"></CMSPRO_CHANNEL>
```

# 获取关联稿件
```html
<CMSPRO_RELDOCUMENTS STARTPOS='0' NUM='5' MODE='ALL'>
    <li>
        <CMSPRO_DOCUMENT field='subTitle' autolink='true' target='_blank' num="100"></CMSPRO_DOCUMENT>
    </li>
</CMSPRO_RELDOCUMENTS>
```

# 面包屑导航
```html
<CMSPRO_LOCATION LINK="&nbsp;&gt;&nbsp;" SELFONLY="false" AUTOLINK="true" TARGET="_blank" LINKEXTRA="" HOMEPAGEDESC="首页">当前位置</CMSPRO_LOCATION>
```

# 来源
```html
<CMSPRO_DOCUMENT FIELD="source" DOMAINMETADATANAME="默认元数据集">信息来源</CMSPRO_DOCUMENT>
```

# 公共头和公共尾
```html
<!--header-->
<!--#include virtual="<CMSPRO_CHANNEL CODE='c104734' FIELD='url'></CMSPRO_CHANNEL>"-->
<!--header end-->
<!-- main -->

<!-- main end -->
<!--footer-->
<!--#include virtual="<CMSPRO_CHANNEL CODE='c104735' FIELD='url'></CMSPRO_CHANNEL>"-->
<!--footer end-->
```

# 自动产生 a 标签
```html
<CMSPRO_CHANNEL CODE="c103022" AUTOLINK="true" LINKALT="true" target="_blank" FIELD="channelName">政府采购</CMSPRO_CHANNEL>
```

# 循环的时候自动编号
```html
<CMSPRO_ROWNO>当前记录序号</CMSPRO_ROWNO>
```

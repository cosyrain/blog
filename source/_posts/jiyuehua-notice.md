---
title: 集约化平台标签注意事项
date: 2021-03-15 15:46:24
categories:
- 集约化平台
toc: true
cover: /gallery/covers/vector_landscape_2.svg
thumbnail: /gallery/covers/vector_landscape_2.svg
---

本篇文章总结了开普集约化平台的各类注意事项。

<!-- more -->

## 文章详情页
页面的时间为 `DATEFORMAT="yyyy-MM-dd HH:mm"` 24小时制，当为 `"yyyy-MM-dd hh:mm"` 时，则为12小时制

## 不同栏目的标签要求

**首页 前3个**

{% codeblock index.html lang:html %}
<meta name="SiteName" content="<CMSPRO_WEBSITE FIELD='name' code=''></CMSPRO_WEBSITE>">
<meta name="SiteDomain" content="www.xinjin.gov.cn"> // <--注意替换
<meta name="SiteIDCode" content="5101320017"> // <--注意替换
{% endcodeblock %}

**列表页 前面7个**

```html list.html
<meta name="ColumnName" content="<CMSPRO_CHANNEL CODE='' FIELD='channelName'></CMSPRO_CHANNEL>">
<meta name="ColumnDescription" content="<CMSPRO_CHANNEL CODE='' FIELD='channelName'></CMSPRO_CHANNEL>">
<meta name="ColumnKeywords" content="<CMSPRO_CHANNEL CODE='' FIELD='channelName'></CMSPRO_CHANNEL>">
<meta name="ColumnType" content="<CMSPRO_CHANNEL CODE='' FIELD='channelName'></CMSPRO_CHANNEL>">
```

**详情页 前面10个**

```html detail.html
<meta name="ArticleTitle" content="<CMSPRO_DOCUMENT FIELD='title' num='100'>标题 </CMSPRO_DOCUMENT>">
<meta name="PubDate" content="<CMSPRO_DOCUMENT field='publishedTime' dateformat='yyyy-MM-dd HH:mm'></CMSPRO_DOCUMENT>">
<meta name="ContentSource" content="<CMSPRO_DOCUMENT FIELD='source' DOMAINMETADATANAME='信息来源'>信息来源</CMSPRO_DOCUMENT>">
```

**详情页 非必需**

<article class="message is-primary" style="font-size:1em">
<div class="message-body">
但是建议都加上，以免后面又变成必须的
</div>
</article>

```html detail.html
<meta name="Keywords" content="<CMSPRO_DOCUMENT FIELD='title' NUM='100'>标题 </CMSPRO_DOCUMENT>">
<meta name="Description" content='<#if cmsInfo.memo?exists>~-!{cmsInfo.memo!""}<#else>~-!{formatHtml(cmsInfo.content?default(""),"50","")}</#if>,' />
```
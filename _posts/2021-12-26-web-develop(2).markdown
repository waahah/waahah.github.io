---
layout:     post
title:      "windows环境下搭建web服务器"
date:       2021-12-26 00:00:00
author:     "waahah"
header-img: "img/post-bg-2015.jpg"
tags:
    - Web
    - 
    - 
---



 <div data-note-content class="show-content">
<h1>写在前面</h1>
   <p> windows环境下如何搭建web服务器，这里也记载一下过程，便于参考。</p>
   <p>至于什么是web服务器，为什么需要web服务器，简单的说就是需要一个能够处理HTTP协议的互联网程序，当做好一个网站后将其放在这个程序包里。如果指定了这个程序所在电脑的IP地址，就可以用浏览器来显示这个网站了。通常这个程序所在的电脑位置我们称之为服务器，而在除了服务器之外的电脑或者移动端我们称之为客户端。在客户端使用网页浏览器，在地址栏输入HTTP://IP地址+文件名，就可以浏览网站了。</p>

<p>目前最主流的三个Web服务器是Apache、Nginx、IIS。Apache是最受欢迎的一款服务器程序，各大互联网公司都有使用它搭建网站，市场占有率接近60%。易安装、易使用，非常受欢迎，但对并发业务处理性能较差。因此Nginx成为了具有大流量、多用户、高并发业务互联网公司搭建服务器时的选择，尤其现在提供云服务的公司。IIS是微软公司提供的一款服务器程序，由windows操作系统自带，实现起来非常简单，功能也比较强大，不过由于微软操作系统本身非开源免费的缘故，市场占有率不如前两种。</p>

<p>下面就windows环境搭建IIS服务步骤简述一下：</p>

<p> 1. 打开控制面板，找到程序，点击卸载程序。</p>


<p> 2. 在卸载程序页面点击启动或关闭windows功能，找到IIS（Internet Information Services）。</p>
    
<p> 3. 如果不考虑更加复杂的web服务器功能，简单实用，直接将IIS左侧的框选中即可。然后点击确定，系统就即将开始安装该服务。完成后，打开系统C盘，就可以看到根目录下多了一个文件夹inetpub。打开该文件夹，里面会有一个wwwroot文件夹，这个文件夹就是放置网站的地方。把做好的网站文件夹放在这个里面，就是网站服务的开始。</p>

<p> 4. 如最开始所示，这个IIS服务就是提供HTTP服务的，如果想要访问网站就还得需要IP地址。如果在本地机器测试，本机的IP地址为127.0.0.1。因此在浏览器地址栏输入http://127.0.0.1/test，这个test就是网站名称。一般情况下都默认直接读取首页，名称为Index开头，如index.html,index.jsp, index.php等；如果要读取网页，即确定的URL，就可以在地址栏输入http://127.0.0.1/test.html。浏览器就会渲染显示test.html文件里的相应的内容。</p>

        </div>

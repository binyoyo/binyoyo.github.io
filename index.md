---
layout: default
title: Binyoyo blog
---
<div class="overlay">
            <div class="log">
              <h1>BINYOYO</h1>
              <h2>woo!..welcome</h2>
              <div class="loging">
                <a href="#">Come in</a>
              </div>
            </div>
</div>
<div class="header">
   <div class="logo">
      <span class="user_image">
        <img src="http://binyoyo.github.io/images/user_image.jpg">
        </span>
        <h1 class="user_name">Binyoyo</h1>
        <span class="user_job">程序猿</span>
    </div><!-- /logo -->

     <div class="nav">
        <ul >
        <li><a href="/" title=".blog" class="active">HOME</a></li>
        <li><a href="/blog" title=".blog">Blog</a></li>
        <li><a href="/life" title=".life">Life</a></li>
        <li><a href="/" title=".me">Me</a></li>
        
        </ul>
   
   </div><!-- /nav -->

</div><!-- /header -->
<div  class="main">
     <div class="blog">
        <h1><a href="/blog">Blog</a></h1>
        <h3><a href="/blog">>>More</a></h3>
        <ul class="article">
        {% for post in site.categories.blog limit:5 %}
        <li>
              <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
              <time>{{ post.date | date:"%B %e, %Y" }}</time>
              <p>{{ post.description }}</p>
        </li>
        {% endfor %}

        <li>
           
     </ul>
    </div><!-- /blog -->
     <div class="life">
        <h1><a href="/life">Life</a></h1>
        <h3><a href="/life">>>More</a></h3>
        <ul class="article">
            {% for post in site.categories.life limit:5 %}
             <li>
             <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
             <time>{{ post.date | date:"%B %e, %Y" }}</time>
             <p>{{ post.description }}</p>
        </li>
        {% endfor %}

        <li>
           
     </ul>
    </div><!-- /life -->
     <div class="me">
        <h1><a href="/">Me</a></h1>
        <div class="aboutme">
          <h2>徐彬</h2>
          <p>binyoyo</p>
          <p>广工计算机学院（俗称'计院'）</p>
          <h2>爱生活、懂感恩、享受生活</h2>
          <p>现阶段最成功的事：我不是单身！woo！哈哈。。。</p>
          <p>每天提醒自己感谢每一个陪伴过你的人</p>
          <p>Qq:160413701</p>
          <p>Email:qqxubin963@gmail.com</p>
          <p>Github:https://github.com/binyoyo</p>
        </div><!-- / -->  
    </div><!-- /what I do -->
</div><!-- /主框架 -->
<script src="js/index.js" ></script>

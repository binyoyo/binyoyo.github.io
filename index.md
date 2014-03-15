---
layout: default
title: Binyoyo blog
---
<link rel="stylesheet" href="css/index.css">
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
        <li><a href=".home" title="" class="active">HOME</a></li>
        <li><a href=".blog" title="">Blog</a></li>
        <li><a href=".life" title="">Life</a></li>
        <li><a href=".me" title="">Me</a></li>
        
        </ul>
   
   </div><!-- /nav -->

</div><!-- /header -->
<div  class="main">
     <div class="home">
        <h1><a href="/">HOME</a></h1>
        <h3><a href="/">>>More</a></h3>
        <ul class="artical">
        {% for post in site.categories.blog limit:4 %}
            <li>
                <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
                <time>{{ post.date | date:"%B %e, %Y" }}</time>
                <p>{{ post.description }}</p>
            </li>
        {% endfor %}
        
     </ul>
    </div><!-- /what I do -->

     <div class="blog">
        <h1><a href="/blog">Blog</a></h1>
        <h3><a href="/blog">>>More</a></h3>
        <ul class="artical">
        {% for post in site.categories.blog limit:4 %}
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
        <ul class="artical">
            {% for post in site.categories.life limit:4 %}
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
        <h1><a href="/me">Me</a></h1>
        <h3><a href="/me">>>More</a></h3>
        <ul class="artical">
        {% for post in site.posts offset:4 limit:4 %}
        <li>
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
        <time>{{ post.date | date:"%B %e, %Y" }}</time>
        {{ post.description }}
        </li>
        {% endfor %}

        <li>
           
     </ul>
    </div><!-- /what I do -->
</div><!-- /主框架 -->

<script src="js/index.js" ></script>
<script src="js/binyoyo.js"></script>

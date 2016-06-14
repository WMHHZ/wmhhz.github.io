---
layout: projects
title: 已完成项目
permalink: /Projects/Completed
---
{% for pro in site.categories.Project %}
{% if pro.jindu == 100 %}
 <div class="jumbotron"> 
   <div class="container"> 
    <div class="row"> 
     <div class="col-md-3"> 
      <div class="thumbnail"> 
       <img style="width: 300px; height: 200px;" alt="300x200" src="{{ pro.logo }}" data-src="holder.js/300x200" /> 
      </div> 
     </div> 
     <div class="col-md-6"> 
      <div class="caption"> 
       <h5>《{{ pro.title }}》</h5> 
       <p>类型：<span class="label label-info smallfont">{{ pro.type }}</span></p> 
       <p>版本：<span class="label label-success smallfont">{{ pro.ver }}</span></p> 
       <p>版本日期：<span class="label label-primary smallfont">{{ pro.time | date: "%Y年%m月%d日" }}</span></p> 
       <p>项目建立日期：<span class="label label-warning smallfont">{{ pro.date | date: "%Y年%m月%d日" }}</span></p>  
      </div> 
     </div> 
     <div class="col-md-3"> 
     <br>
     <br>
      <p>汉化进度：</p> 
      <div class="progress"> 
      {% if  pro.jindu == 100 %}
       <div class="progress-bar progress-bar-success" style="width: {{ pro.jindu }}%;">已完成</div>    
       {% endif %}
       {% if 59 < pro.jindu < 100 %}
       <div class="progress-bar" style="width: {{ pro.jindu }}%;">{{ pro.jindu }}%</div>  
       {% endif %}
       {% if 0 < pro.jindu < 60 %}
       <div class="progress-bar progress-bar-warning" style="width: {{ pro.jindu }}%;">{{ pro.jindu }}%</div>
       {% endif %}
       {% if  pro.jindu == 0 %}
       <div class="progress-bar progress-bar-warning" style="width: {{ pro.jindu }}%;">无</div>
       {% endif %}
      </div> 
       <a class="btn btn-inverse" href="{{ pro.url }}"><span class="glyphicon glyphicon-align-justify" aria-hidden="true">　</span>点击进入项目页</a>
     </div> 
    </div> 
   </div>
  </div>
{% endif %}
{% endfor %}
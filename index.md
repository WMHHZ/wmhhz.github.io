---
layout: default
---
{% for tip in site.topic %}
<div class="panel panel-primary visible-xs-block">
      <div class="panel-heading">
        <h3 class="panel-title smallfont">{{ tip.title }}</h3>
      </div>
      <div class="panel-body smallfont">
        {{ tip.text }}
      </div>
    </div>
{% endfor %}

<div class="alert alert-warning smallfont  visible-xs-block">
  <button type="button" class="close" data-dismiss="alert" aria-label="Close"><span aria-hidden="true">&times;</span></button>
<strong>提示：</strong>
当前为移动终端或小屏设备访问，资源下载将受到影响，请更换电脑访问本站。
</div>

<div class="panel panel-success visible-xs-block">
      <div class="panel-heading">
        <h3 class="panel-title smallfont">{{ site.string.topic2 }}</h3>
      </div>
      <div class="panel-body">
      {% for tip in site.topic2 %}
      <div class="alert alert-success smallfont">
        <a href="{{ tip.text }}">{{ tip.title }}</a><br>
        </div>
        {% endfor %}
      </div>
    </div>
    
<div id="carousel-example-generic" class="carousel slide hidden-xs" data-ride="carousel">
  <!-- Indicators -->
  <ol class="carousel-indicators">
    <li data-target="#carousel-example-generic" data-slide-to="0" class="active"></li>
  </ol>

  <!-- Wrapper for slides -->
  <div class="carousel-inner" role="listbox">
    <div class="item active">
      <img src="/img/wm.jpg" alt="INDEX">
      <div class="carousel-caption">
        <a class="btn btn-info btn-sm" href="/About">了解无名汉化组</a>　<a class="btn btn-info btn-sm" href="/Projects">查看无名汉化组汉化项目</a>
        <p class="smallfont" >无名汉化组系一群游戏爱好者组成的汉化组织，成立于2012年。</p>
      </div>
    </div>
  </div>

  <!-- Controls -->
  <a class="left carousel-control" href="#carousel-example-generic" role="button" data-slide="prev">
    <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
    <span class="sr-only">上一页</span>
  </a>
  <a class="right carousel-control" href="#carousel-example-generic" role="button" data-slide="next">
    <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
    <span class="sr-only">下一页</span>
  </a>
</div>
<br>

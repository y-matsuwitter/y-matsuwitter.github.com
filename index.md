---
layout: page
title: memo
tagline: y-matuwitterさんのチラシの裏的なアレ。
---
{% include JB/setup %}
<div class="span9">
{% for post in site.posts limit:5 %}
  <div>
    <span>{{ post.date | date: "%Y/%m/%d" }}</span>
    <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
    <div class="social">
      <div class="fb-like" data-href="{{ site.production_url }}{{ post.url }}" data-send="false" data-layout="button_count" data-width="450" data-show-faces="false">
      </div>
      <a href="http://b.hatena.ne.jp/entry/{{ site.production_url }}{{ post.url }}" class="hatena-bookmark-button" data-hatena-bookmark-title="{{ post.title }}" data-hatena-bookmark-layout="simple-balloon" title="このエントリーをはてなブックマークに追加">
        <img src="http://b.st-hatena.com/images/entry-button/button-only.gif" alt="このエントリーをはてなブックマークに追加" width="20" height="20" style="border: none;" />
      </a>
      <script type="text/javascript" src="http://b.st-hatena.com/js/bookmark_button.js" charset="utf-8" async="async">
      </script>
      <a href="{{ site.production_url }}{{ post.url }}" data-url="{{ site.production_url }}{{ post.url }}" class="twitter-share-button" data-text="{{post.title}} - y_matsuwitter.memo" data-lang="ja" data-hashtags="#ym-memo">Tweet</a>
      <script>
        !function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src="https://platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");
      </script>
    </div>
    <p>{{ post.content }}</p>
  </div>
{% endfor %}
</div>

<div class="span1">
  <ul class="menu">
    <li>Archive</li>
    <li>Category</li>
    <li>Pages</li>
    <li>Tags</li>
  </ul>
</div>

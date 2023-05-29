---
layout: gridlay
title: News
subtitle: Neurophysiology and Neuroengineering Lab News
---

# **News**
{% for item in site.data.News %}
<hr>
<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div id = "{{item.title}}" class="row" style="padding-top: 60px; margin-top: -60px;">
    <div class="col-sm-4">
    	<a><img src="{{item.image}}" alt="{{item.title}}"></a>
    </div>
    <div class="col-sm-8" style="text-align: justify">
    	<h5>{{item.title}}</h5>
    	{{item.description| markdownify}}
    </div>
</div>
{% endfor %}

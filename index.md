---
#
# By default, content added below the "---" mark will appear in the home page
# between the top bar and the list of recent posts.
# To change the home page layout, edit the _layouts/home.html file.
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: post_v2
title: Home
---


<div class = "something">
{% for projects in site.projects %}
{% if projects.category != "test"%}
<a href="{{projects.url}}"  class = "somethingelse" >
    <div class = "imageholder" style = " background-image: url({{projects.thumbnail}});  background-size: cover; background-repeat: no-repeat; background-position: center center;">
    </div>
<div class = "contentholder">

<div class = "content">
  <h1>
    
      {{projects.title}} 
    
  </h1>
  <p>{{ projects.summary | markdownify }}</p>
</div>
</div>
</a>
{% endif %}
{% endfor %}
</div>








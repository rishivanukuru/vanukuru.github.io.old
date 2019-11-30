---
layout: post
permalink: /paperholder/
---

<h1>Heading One</h1>
<div class = "something">
{% for papers in site.papers %}  
  <div class = "somethingelse" style = " background-image: url({{papers.image_path}}); ">
  <h2>
    <a href="/compendium{{papers.url}}" target = "_blank">
      {{papers.title}} 
    </a>
  </h2>
  <p>{{ papers.summary | markdownify }}</p>
  </div>
{% endfor %}
</div>

<h1>Heading Two</h1>
<div class = "something">
{% for papers in site.papers %}
    
    {% if papers.category == 'test' %}
        
        <div class = "somethingelse" style = " background-image: url({{papers.image_path}}); ">
        <h2>
            <a href="/compendium{{papers.url}}" target = "_blank">
            {{papers.title}} 
            </a>
        </h2>
        <p>{{ papers.summary | markdownify }}</p>
        </div>
  
    {% endif %}
  
{% endfor %}
</div>
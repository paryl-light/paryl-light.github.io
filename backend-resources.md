---
layout: page
title: Resources for Backend Developers.
image: 
page_id: '2'
meta_title: Resources for Backend Developers.
meta_description: A place to find information for backend developers.
---
{% capture index %}{% include pages/backend-developers.md %}{% endcapture %}
{{ index | markdownify }}

(Temporary, please excuse me while I update styles and content!)

<ul>
{% assign catResources = site.data.resources | where, "category", "mtf"  %}
{% for resource in catResources %}
    <li>
        <a href="{{resource.url}}" title="{{resource.description}}" class="color-{{resource.category}};">{{resource.name}}</a>
    </li>
{% endfor %}
{% assign catResources = site.data.resources | where, "category", "general"  %}
{% for resource in catResources %}
    <li>
        <a href="{{resource.url}}" title="{{resource.description}}" style="color: {{resource.color}};">{{resource.name}}</a>
    </li>
{% endfor %}
</ul>
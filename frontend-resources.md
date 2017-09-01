---
layout: page
title: Resources for Frontend Developers
image: 
page_id: '3'
meta_title: Resources for Frontend Developers
meta_description: A bunch of resources for Frontend Developers.
---
{% capture page %}{% include pages/frontend-resources.md %}{% endcapture %}
{{ index | markdownify }}

(Temporary, please excuse me while I update styles and content!)

<ul>
{% assign catResources = site.data.resources | where, "category", "ftm"  %}
{% for resource in catResources %}
    <li>
        <a href="{{resource.url}}" title="{{resource.description}}" style="color: {{resource.color}};">{{resource.name}}</a>
    </li>
{% endfor %}
{% assign catResources = site.data.resources | where, "category", "general"  %}
{% for resource in catResources %}
    <li>
        <a href="{{resource.url}}" title="{{resource.description}}" style="color: {{resource.color}};">{{resource.name}}</a>
    </li>
{% endfor %}
</ul>
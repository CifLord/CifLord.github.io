--- layout: archive title: "News" permalink: /news/ author_profile: true --- {% include base_path %} {% if site.news_category %} {% for category in site.news_category %} {% assign title_shown = false %} {% for post in site.news reversed %} {% if post.category != category[0] %} {% continue %} {% endif %} {% unless title_shown %}
{{ category[1].title }}

{% assign title_shown = true %} {% endunless %} {% include archive-single.html %} {% endfor %} {% endfor %} {% else %} {% for post in site.news reversed %} {% include archive-single.html %} {% endfor %} {% endif %}
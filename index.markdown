---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

# {{ site.title }}

{{ site.description }}

{% assign categories = "linux" | split: "," %}

{% for category in categories %}
## {{ category | capitalize }}

{% for post in site.categories[category] %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}

{% endfor %}

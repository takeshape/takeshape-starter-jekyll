---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults, thanks.

layout: home
---

<ul>
{% graphql endpoint: "takeshape", query: "getProductList" %}
  {% for product in data["getProductList"]["items"] %}
    <li>
        {{product["name"]}} Price:
        <em>{{product["price"]}}</em>
    </li>
  {% endfor %}
{% endgraphql %}
</ul>
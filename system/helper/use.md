# Use

### Use helper in block or field templates

{% tabs %}
{% tab title="TWIG" %}
```markup
{% set menu = linotype.helper.Menu.get({'data':[]}) %}

{% for item in menu %}
    <a href="{{item.path}}">{{item.name}}</a>
{% endfor %}
```
{% endtab %}

{% tab title="PHP" %}
```
TODO
```
{% endtab %}
{% endtabs %}




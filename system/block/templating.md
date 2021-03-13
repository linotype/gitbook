---
description: linotype/Block
---

# Templating

The **template** of a block allows you to code a **piece of your site**. Lots of **variables** and **functions** are available to make your template **powerful**.

### Default variables

{% tabs %}
{% tab title="TWIG" %}
```markup
<div id="{{block.id}}" uid="{{block.uid}}" class="{{block.class}}">
    <h1>Hello world !</h1>
    {{childrens}}
<div>
```
{% endtab %}

{% tab title="PHP" %}
```
TODO
```
{% endtab %}

{% tab title="JSX" %}
```
TODO with v8js ssr
```
{% endtab %}
{% endtabs %}

| variable | description |
| :--- | :--- |
| {{block.id}}  | Unique block ID: \#block--**block\_key** |
| {{block.uid}} | Unique block ID: \#md5\(_themeKey\_\_templateKey\_\_blockKey\)_ |
| {{block.class}} | Class id .block--**block\_id** |
| {{block.childrens}} | Array of childrens defined in module or template config |
| {{childrens}} | Rendered childrens define in module or template config |

### Context variables

Use your context key just like variables. Their values change depending on the configuration and where the block is used.

{% tabs %}
{% tab title="TWIG" %}
```markup
{% if context_id_1 and context_id_2 %}
    <div id="{{block.id}}" uid="{{block.uid}}" class="{{block.class}}">
        {{context_id_1}}
        {{context_id_2}}
    <div>
{% endif %}
```
{% endtab %}

{% tab title="PHP" %}
```
TODO
```
{% endtab %}

{% tab title="JSX" %}
```
TODO with v8js ssr
```
{% endtab %}
{% endtabs %}

### Functions helper

Create a [helper](../helper/structure.md) and use them in your template to enrich your content.

{% tabs %}
{% tab title="TWIG" %}
```markup
{% set title = linotype.helper.format.removeTags( text ) %}

<div id="{{block.id}}" uid="{{block.uid}}" class="{{block.class}}">
    <h1>{{title}}</h1>
<div>
```
{% endtab %}

{% tab title="PHP" %}
```
TODO
```
{% endtab %}

{% tab title="JSX" %}
```
TODO with v8js ssr
```
{% endtab %}
{% endtabs %}


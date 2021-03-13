---
description: linotype/Block
---

# Exemple

### Title.yml 

This is a config yaml exemple for a basic block title

{% tabs %}
{% tab title="YAML" %}
```yaml
block:

  version: 1.0
  author: ynk 
 
  name: Title
  desc: Create a simple title
  
  context:

    title:
      field: Text
      option:
        placeholder: The title
      value: null
      default: My template title
      preview: Lorem ipusum
      debug: false
      js: true

    style:
      field: Static
      value: text-big
      
    color:
      field: Static
      value: red
      css: true
```
{% endtab %}
{% endtabs %}

### Title.twig

This is a twig exemple, but you can use php version \( or html with js wrapper \)

{% tabs %}
{% tab title="TWIG" %}
```markup
<div id="{{block.id}}" uid="{{block.uid}}" class="{{block.class}}" data-controller="title">
    <h1 class="{{style}}">{{title}}</h1>
<div>
```
{% endtab %}
{% endtabs %}

### Title.scss

This is a scss exemple, but you are free to use simple css 

{% tabs %}
{% tab title="SCSS" %}
```css
.block--title {
    h1 {
        font-size:2rem;
        color: var(--color);
        &.text-big {
            font-size:3rem;
        }
    }
}
```
{% endtab %}
{% endtabs %}

### Title.js 

This is a stimulus.js exemple, but you are free to use vanilla.js

{% tabs %}
{% tab title="Stimulus" %}
```javascript
import { Controller } from "stimulus"

export default class extends Controller {

  connect() {
  
    let block = this.element;
    let uid = block.getAttribute("uid");
    let data = linotype[uid];
    
    console.log("Title value is: " + data.value )
  
  }
  
}
```
{% endtab %}
{% endtabs %}


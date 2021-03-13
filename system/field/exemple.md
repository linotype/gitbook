---
description: linotype/Field
---

# Exemple

### Text.yml

This is a config yaml exemple for a basic field text

{% tabs %}
{% tab title="YAML" %}
```yaml
field:

  version: 1.0 
  package: ynk

  name: Text
  desc: Text field
  
  option:
    placeholder: ...

  format:
    type: long_text
  
```
{% endtab %}

{% tab title="Help" %}
```yaml
field:

  version: 1.0 #the field version 
  package: ynk #the field package 
  
  name: Text #display block name
  desc: Text field #display block description
  
  option: #create option for field
    placeholder: ... #option exemple

  format: #format value before save
    type: long_text #database type
    
```
{% endtab %}
{% endtabs %}

### Text.twig

This is a twig exemple, but you can use php version \( or html with js wrapper \)

{% tabs %}
{% tab title="TWIG" %}
```markup
<div id="{{field.id}}" class="{{field.class}}">
    <input placeholder="{{option.placeholder}}" value="{{field.value}}"/>
</div>
```
{% endtab %}

{% tab title="PHP" %}
```
soon
```
{% endtab %}

{% tab title="HTML" %}
```
soon
```
{% endtab %}
{% endtabs %}

### Text.scss

This is a scss exemple, but you are free to use simple css 

{% tabs %}
{% tab title="SCSS" %}
```css
.Text {
    input {
        background:#DDD;
        color:#333;
    }
}
```
{% endtab %}

{% tab title="CSS" %}
```css
.Text  input {
    background:#DDD;
    color:#333;
}
```
{% endtab %}
{% endtabs %}

### Text.js 

This is a stimulus.js exemple, but you are free to use vanilla.js

{% tabs %}
{% tab title="Stimulus" %}
```javascript
import { Controller } from "stimulus"

export default class extends Controller {
  connect() {
    console.log("Text field loaded", this.element)
  }
}
```
{% endtab %}

{% tab title="Vanilla" %}
```javascript
(function (linotype) {

  var blocks = document.getElementsByClassName("Text");

  for ( var i = 0; i < blocks.length; i++ ) {

    blocks[i].onclick = function() {
      console.log('Text: click');
    }
    
  }

})(linotype)
```
{% endtab %}

{% tab title="jQuery" %}
```javascript
(($) => {

  $(function() {
    
    const id = 'Text';

    const el = $(id);
    
    if ( el.length ) el.each(init);

    function init( item, index ) 
    {  
      console.log( id, index, item );
    }

  })

})(jQuery)
```
{% endtab %}

{% tab title="React" %}
```
TODO
```
{% endtab %}
{% endtabs %}




---
description: linotype/Block
---

# Javascript

Each block has an associated javascript code. You can add your scripts in the following ways. Define the one you use in the global [linotype](../linotype.yml/global.md) configuration

{% tabs %}
{% tab title="Stimulus" %}
```javascript
import { Controller } from "stimulus"

export default class extends Controller {

  initialize(){}
  
  connect() {
  
    let block = this.element;
    let uid = block.getAttribute("uid");
    let data = linotype[uid];
    
    console.log("block--block_id", block, data )
  
  }
  
  disconnect(){}
  
}
```
{% endtab %}

{% tab title="Vanilla" %}
```javascript
(function (linotype) {

  var blocks = document.getElementsByClassName("block--block_id");

  for ( var i = 0; i < blocks.length; i++ ) {
    
    var block = blocks[i];
    var uid = block.getAttribute("uid");
    var data = linotype[uid];
    
    console.log("block--block_id", block, data )
    
  }

})(linotype)
```
{% endtab %}

{% tab title="jQuery" %}
```javascript
(($, linotype) => {

  $(function() {
    
    const id = 'block--block_id';

    const el = $(id);
    
    if ( el.length ) el.each(init);

    function init( item, index ) 
    {  
      var block = blocks[i];
      var uid = block.getAttribute("uid");
      var data = linotype[uid];
    
      console.log( id, index, item );
    }

  })

})(jQuery, linotype)
```
{% endtab %}

{% tab title="React" %}
```
TODO
```
{% endtab %}
{% endtabs %}

**linotype:** this global variable server side generated data


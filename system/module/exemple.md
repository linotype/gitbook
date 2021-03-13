---
description: linotype/Module
---

# Exemple

### Header.yml

This is a config yaml exemple for a basic module header

{% tabs %}
{% tab title="YAML" %}
```yaml
module:

  version: 1.0
  package: ynk
  
  name: Header
  desc: Display header

  layout:
    
    toolbar:
      block: Toolbar
      
    sitename:
      block: Title
      override:
        - title/field: Static
        - title/value: My website
    
    menu:
      block: Menu
      
```
{% endtab %}

{% tab title="Help" %}
```yaml
group:

  version: 1.0 #the header version 
  package: ynk #the header package 
   
  name: Header #display block name
  desc: Display header #display block description

  layout: #list of blocks
    
    toolbar: #block unique id
      block: Toolbar #exemple of block
      
    sitename: #block unique id
      block: Title #block loaded
      override: #override specifique context
        - title/field: Static
        - title/value: My website
    
    menu: #block unique id
      block: Menu #exemple of block
      
```
{% endtab %}
{% endtabs %}




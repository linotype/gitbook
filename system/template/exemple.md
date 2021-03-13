---
description: linotype/Template
---

# Exemple

### Page.yml

This is a config yaml exemple for a basic template page

{% tabs %}
{% tab title="YAML" %}
```yaml
template:

  version: 1.0
  package: ynk
  
  name: Page
  desc: Page with header & footer
  
  layout:

    header:
      module: Header

    content:
      block: Title
      override:
        - text/field: Static
        - text/value: Use block with static override

    footer:
      module: Footer
        override:
          - poweredby/text/value: powered by linotype

```
{% endtab %}

{% tab title="Help" %}
```yaml
template:

  version: 1.0 #the header version 
  package: ynk #the header package 
  
  name: Page #display template name
  desc: Page with header & footer #display template description
  
  layout: #list blocks and groups

    header: #unique group id
      group: Header #group to load

    content: #unique block id
      block: Title #block to load
      override: #overide block context
        - text/field: Static
        - text/value: Use block with static override

    footer:
      group: Footer #group to load
        override: #overide group context
          - poweredby/text/value: powered by linotype
          
```
{% endtab %}
{% endtabs %}




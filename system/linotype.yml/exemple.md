---
description: linotype/linotype.yml
---

# Exemple

### linotype.yml

{% tabs %}
{% tab title="YAML" %}
```yaml
linotype:
  version: 1.0 
  debug: false
  preview: false
  script: stimulus
  style: scss
  theme: Default
  
  # sites:

  #   demo:
  #     domain: www.demo.com
  #     theme: Default

  #   futuroscope:
  #     domain: www.futuroscope.com
  #     theme: Futuroscope

  #   peclersplus:
  #     domain: peclers.fr
  #     theme: Peclers

```
{% endtab %}

{% tab title="Help" %}
```yaml
linotype:
  version: 1.0 #project version
  debug: false #active debug panel
  preview: false #use preview value for front integration without data
  script: stimulus #use javascript type
  style: scss #select style type
  theme: Default #active current theme
  
  sites: #TODO: multisite manager
```
{% endtab %}
{% endtabs %}




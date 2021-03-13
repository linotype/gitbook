---
description: linotype/Helper
---

# Exemple

### Menu.yml

This is a config yaml exemple for a basic helper header

{% tabs %}
{% tab title="YAML" %}
```yaml
helper:

  version: 1.0
  package: ynk
  
  name: Menu
  desc: Get menu from theme map
  
  methodes:

    getMenuItems:
      title: Get Custom data
      desc: Return array of custom data
      controller: 'App\Service\Menu\MenuService::getMenuItems'
      tags: ['controller.service_arguments']
```
{% endtab %}

{% tab title="Help" %}
```

```
{% endtab %}
{% endtabs %}




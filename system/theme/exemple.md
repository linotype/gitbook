---
description: linotype/Theme
---

# Exemple

### Default.yml

This is a config yaml exemple for a basic theme 

{% tabs %}
{% tab title="YAML" %}
```yaml
theme:
  
  version: 1.0
  package: ynk
  
  name: Default
  desc: Default theme

  map:
    
    home:
      single:
        path: /
        template: Page
        public: true

    article:
      archive:
        path: /articles
        template: Articles
        public: true
      single:
        path: /article/{id}
        template: Article
        public: true

    contact:
      single:
        path: /contact
        template: Form
        public: true
        override:
          - form/form_id: contact
            
    quote:
      single:
        path: /quote
        template: Form
        public: true
        override:
          - form/form_id: quote
    
    test:
      single:
        path: /test 
        template: Test
        public: false

```
{% endtab %}
{% endtabs %}


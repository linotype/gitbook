---
description: linotype/Block
---

# Stylesheet

Each block has an associated stylesheet code. You can add your style in the following ways. Define the one you use in the global [linotype](../linotype.yml/global.md) configuration

{% tabs %}
{% tab title="SCSS" %}
```css
.block--block_id {
    h1 {
        font-size:2rem;
        &.text-big {
            font-size: var(--context_id_4);
        }
    }
}
```
{% endtab %}

{% tab title="CSS" %}
```css
.block--block_id h1 {
    font-size:2rem;
}
.block--block_id h1.text-big {
    font-size: var(--context_id_4);
}
```
{% endtab %}
{% endtabs %}

### 


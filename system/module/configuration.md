---
description: linotype/Module
---

# Configuration

Define an array with **module** key and the following datas: 

| key | type | require | default |
| :--- | :--- | :--- | :--- |
| [version](../theme/structure.md#version) | string | true | 1.0 |
| [package](../theme/structure.md#package) | string | true |  |
| [name](../theme/structure.md#name) | string | true | Unknow |
| [desc](../theme/structure.md#desc) | string | true | Unknow |
| [layout](structure.md#layout) | array | false |  |

### version

The version is used to be notified in the linotype tools if a new version of the module is available. You need to configure linotype [sync](../../tools/sync.md) systeme.

```yaml
version: 1.0
```

### author

The author is the repository reference to the block. Like **linotype/slider**

```yaml
author: linotype
```

### name

Define a theme name displayed in the linotype tools

```yaml
name: Header
```

### desc

Define a theme description displayed in the linotype tools

```yaml
desc: The header website with title and menu
```

### layout

the module layout part is a list of blocks that you can use multiple time in your templates.

```yaml
layout:
      
    block_id_1:
      block: Title
      override:
        - title/field: Static
        - title/value: My website
    
    block_id_2:
      block: Menu
        
        
```

| key | description | type | require | default |
| :--- | :--- | :--- | :--- | :--- |
| block | The block ID to use in the module | string | no | Static |
| override | List of block value to override from the module | array | no | null |
| debug | Display a debug panel above the module in the template | boolean | no | false |

**block\_id\_1:** By default, this block has an auto-generates field for the backend. Use the override option to define a value and use this block with static data only in this module.


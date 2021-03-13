---
description: linotype/Helper
---

# Configuration

Define an array with **helper** key and the following datas: 

| key | type | require | default |
| :--- | :--- | :--- | :--- |
| [version](../theme/structure.md#version) | string | true | 1.0 |
| [package](../theme/structure.md#package) | string | true |  |
| [name](../theme/structure.md#name) | string | true | Unknow |
| [desc](../theme/structure.md#desc) | string | true | Unknow |

### version

The version is used to be notified in the linotype tools if a new version of the block is available. You need to configure linotype [sync](../../tools/sync.md) systeme.

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
name: Slider
```

### desc

Define a theme description displayed in the linotype tools

```yaml
desc: Display a simple photo slider
```


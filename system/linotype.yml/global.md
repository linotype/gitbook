---
description: linotype/linotype.yml
---

# Configuration

Define an array with **linotype** key and the following values: 

| key | type | require | default |
| :--- | :--- | :--- | :--- |
| xxx | string | true | 1.0 |

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


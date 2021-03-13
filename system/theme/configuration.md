---
description: linotype/Theme
---

# Configuration

Define an array with **theme** key and the following datas: 

| key | type | require | default |
| :--- | :--- | :--- | :--- |
| [version](structure.md#version) | string | true | 1.0 |
| [package](structure.md#package) | string | true |  |
| [name](structure.md#name) | string | true | Unknow |
| [desc](structure.md#desc) | string | true | Unknow |
| [map]() | array | false |  |

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

### Map

Define an array with key and the following datas.

| key | type | require | default |
| :--- | :--- | :--- | :--- |
| path | string | true | / |
| type | string | true | single |
| template | string | true |  |
| public | boolean | false | true |
| entity | array | false |  |


---
description: linotype/Block
---

# Configuration

Start your MyBlock.yml file with the array key **block** and add the following values: 

| key | type | require | default |
| :--- | :--- | :--- | :--- |
| [version](configuration.md#version) | string | yes | 1.0 |
| [author](configuration.md#author) | string | yes | local |
| [name](configuration.md#name) | string | yes | unknow |
| [desc](configuration.md#desc) | string | yes | unknow |
| [package](configuration.md#package) | array | no | null |
| [parent](configuration.md#parent) | string/array | no | ~ |
| [accept](configuration.md#accept) | string/array | no | all |
| [context](configuration.md#context) | array | no | null |

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

### package

List of require **node\_modules** for the block. Auto npm/yarn install on linotype command install/update

```yaml
package:
    - "swiper": "6.4.11"
    - ...
```

### parent

Define where the block can be used. Sometimes your block is a subpart of another block. This parameter allows you to define which block can use it as a child.

```yaml
parent: ~ #root
-or-
parent: block_id
-or-
parent:
    - block_id
    - ...
```

### accept

If your block is a subpart of another block. This parameter allows you to define which block can add it as children.

```yaml
accept: all
-or-
accept: block_id
-or-
accept:
    - block_id
    - ...
```

### context

the context part is a list of variables that you can use in your template, script, and style. Each variable has a set of parameters to define its value and create the admin version of the block. 

```yaml
context:
    
    context_id_1:
        name: Welcome text
        desc: Display Hello with name from contribution
        field: Text
        persist: meta
        option:
            placeholder: Your name here
        default: Yannick
        preview: John Doe
        format: Hello <b>{{value}}</b>!
        debug: false
    
    context_id_2:
        name: Title
        desc: Simple static text value
        field: Static
        default: My static value
        js: true
        
    context_id_3:
        name: Link value
        field: Link
        persist: option
        default: {
            "link": "https://linotype.dev", 
            "title": "linotype"
        } 
        format: <a href="{{value.title}}">{{value.link}}</a>
        
    context_id_4:
        name: Font Size
        value: 3rem
        css: true
        
```

| key | description | type | require | default |
| :--- | :--- | :--- | :--- | :--- |
| name | The context name | string | yes | Unknow |
| desc | The context description | string | no | empty |
| field | The field ID used to format and edit the value in admin mode | string | no | Static |
| persist | Save context as template meta or global option | string | no | meta |
| option | The field options \(check in relative field yaml config file\) | array | no | null |
| value | Force the value as static \(usefull from template or module override\) | string | no | empty |
| default | The default value if no contribution | string | no | empty |
| preview | The value used in preview mode | string | no | empty |
| format | If value return data, format data with custom content. If data is json, value return an array of variable |  |  |  |
| debug | Display a debug panel above the block in the template | boolean | no | false |
| js | Add to global linotype inline javascript variable | boolean | no | false |
| css | Add to global linotype inline css variable | boolean | no | false |

**context\_id\_1:** This context automatically generates a backend field when used in a module or template . You can replace the value of the field with 'stratic' to disable the automatic generation field from the backend and assign a value to it by replacing the 'value' or 'default'. 

**context\_id\_2:** This context is a static value, no backend generated when the block is used in a module or template. You can make it dynamic from the module or template by overriding the field value with a field id and also your can override the field options.

**context\_id\_3:** If you create a custom field that save json data, you get array in the formater


# Standalone

## Installation steps

{% hint style="danger" %}
**linotype standalone** is not yet usable
{% endhint %}

Create new composer project:

```
$ composer init
```

Add composer extra installer & paths to import linotype project \(for next step\):

{% code title="\[edit\] composer.json" %}
```javascript
{
    "extra": {
        "installer-types": ["linotype"],
        "installer-paths": {
            "linotype/": ["type:linotype"]
        }
    }
}
```
{% endcode %}

Install linotype core with composer from the packagist.org repository:

{% tabs %}
{% tab title="Production" %}
```
$ composer require linotype/core
```
{% endtab %}

{% tab title="Develop" %}
```
$ composer require linotype/core "v1.x-dev" --dev --no-cache
```
{% endtab %}
{% endtabs %}

Add linotype project sample from repository \(e.g. official starter\):

{% tabs %}
{% tab title="Production" %}
```
$ composer require linotype/starter
```
{% endtab %}

{% tab title="Develop" %}
```
$ composer require linotype/starter "v1.x-dev" --dev --no-cache
```
{% endtab %}
{% endtabs %}

Build assets:

```text
$ yarn --cwd linotype/Base build
```



{% hint style="success" %}
**Done! You are ready to create your first linotype powered website**
{% endhint %}

\*\*\*\*


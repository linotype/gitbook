# Standalone

## Installation steps

{% hint style="danger" %}
**linotype standalone** is not yet usable
{% endhint %}

### Create new composer project:

```
composer init
```

### Install linotype:

{% tabs %}
{% tab title="v1.1" %}
Require linotype core with composer from the packagist.org repository:

```
composer require linotype/core
```

Add linotype project sample from repository \(e.g. official starter\):

```text
composer require linotype/starter
```
{% endtab %}

{% tab title="v1.x-dev" %}
Install from v1.x-dev branch:

```
composer require linotype/core:v1.x-dev linotype/starter:v1.x-dev --dev --no-cache         
```
{% endtab %}
{% endtabs %}

### Build:

```text
yarn --cwd linotype/Base build
```



{% hint style="success" %}
**Done! You are ready to create your first linotype powered website**
{% endhint %}

\*\*\*\*


# Standalone

## Installation steps

{% hint style="danger" %}
**linotype standalone** is not yet usable
{% endhint %}

### Create new composer project:

```text
composer init
```

### Install linotype:

{% tabs %}
{% tab title="v1.1" %}
Require linotype core with composer from the packagist.org repository:

```text
composer require linotype/linotype
```

Add linotype project sample from repository \(e.g. official starter\):

```text
composer require linotype/starter
```
{% endtab %}

{% tab title="v1.x-dev" %}
Install from v1.x-dev branch:

```text
composer require linotype/linotype:v1.x-dev linotype/starter:v1.x-dev --dev --no-cache
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

Learn more about using linotype in the [standalone environment](../environement/standalone.md).


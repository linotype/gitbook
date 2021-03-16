# Symfony

## Installation steps

{% hint style="success" %}
**linotype for symfony** is under development, **but** **you can give a try with develop tabs bellow**
{% endhint %}

Create new symfony project:

```
$ symfony new my_website
```

Install linotype:

{% tabs %}
{% tab title="Common" %}
Require linotype bundle with composer from the packagist.org repository:

```
$ composer require linotype/symfony
```

Add linotype project sample from repository \(e.g. official starter\):

```text
$ composer require linotype/starter
```
{% endtab %}

{% tab title="Develop" %}
Install from v1.x-dev branch:

```
$ composer require linotype/symfony linotype/core linotype/installers linotype/starter v1.x-dev --dev --no-cache$ composer require linotype/starter "v1.x-dev" --dev --no-cache
```
{% endtab %}
{% endtabs %}

Change default twig path to linotype _\(flex recipe comming soon\):_

{% code title="\[edit\] config/packages/twig.yaml" %}
```yaml
twig:
    default_path: '%kernel.project_dir%/linotype'
```
{% endcode %}

Add linotype route config _\(flex recipe comming soon\):_

{% code title="\[create\] config/routes/linotype.yaml" %}
```yaml
linotype:
  resource: '@LinotypeBundle/Resources/config/routes.yaml'
```
{% endcode %}

Choose and configure a database provider in doctrine:

{% code title="\[edit\] .env" %}
```text
###> doctrine/doctrine-bundle ###
# Format described at https://www.doctrine-project.org/projects/doctrine-dbal/en/latest/reference/configuration.html#connecting-using-a-url
# IMPORTANT: You MUST configure your server version, either here or in config/packages/doctrine.yaml
#
DATABASE_URL="sqlite:///%kernel.project_dir%/var/data.db"
# DATABASE_URL="mysql://db_user:db_password@127.0.0.1:3306/db_name?serverVersion=5.7"
# DATABASE_URL="postgresql://db_user:db_password@127.0.0.1:5432/db_name?serverVersion=13&charset=utf8"
###< doctrine/doctrine-bundle ###
```
{% endcode %}

Execute common symfony command _\(flex recipe comming soon\):_

```text
$ symfony console make:migration

$ symfony console doctrine:migrations:migrate

$ symfony console clear:cache
```

Start local server and build assets:

```text
$ symfony serve
$ yarn --cwd linotype/Base build
```



{% hint style="success" %}
**Done! You are ready to create your first linotype powered website**
{% endhint %}

\*\*\*\*

**Check more information for symfony use in environements section:**

{% page-ref page="../environement/symfony.md" %}








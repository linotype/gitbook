# Symfony

## Installation steps

{% hint style="success" %}
**linotype for symfony** is under development, ****prefer the linotype **v1.x-dev** install
{% endhint %}

### Create new symfony project:

```
symfony new my_website        
```

### Install linotype:

{% tabs %}
{% tab title="v1.1" %}
Require linotype bundle with composer from the packagist.org repository:

```
composer require linotype/symfony        
```

Add a linotype starter project from repository \(default starter bellow, **choose another one** [here](../exemple/)\):

```text
composer require linotype/starter        
```
{% endtab %}

{% tab title="v1.x-dev" %}
Install from v1.x-dev branch:

```
composer require linotype/symfony:v1.x-dev linotype/core:v1.x-dev linotype/installers:v1.x-dev linotype/starter:v1.x-dev --no-cache           
```
{% endtab %}
{% endtabs %}

### Configure symfony _\(flex recipe comming soon\)_

#### Change default twig path to linotype_:_

{% code title="\[edit\] config/packages/twig.yaml" %}
```yaml
twig:
    default_path: '%kernel.project_dir%/linotype'        
```
{% endcode %}

#### Create linotype route config_:_

{% code title="\[create\] config/routes/linotype.yaml" %}
```yaml
linotype:
  resource: '@LinotypeBundle/Resources/config/routes.yaml'        
```
{% endcode %}

### Setup the database provider

#### Choose and configure a database provider in doctrine:

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

#### Execute common symfony command_:_

```text
symfony console make:migration        
```

```text
symfony console doctrine:migrations:migrate        
```

```text
symfony console cache:clear        
```

### Run local environement

#### Serve and build assets:

```text
symfony serve        
```

```text
yarn --cwd linotype/Base install       
```

```text
yarn --cwd linotype/Base build        
```

{% hint style="success" %}
**Done! You are ready to create your first linotype powered website**
{% endhint %}

Learn more about using linotype in the [symfony environment](../environement/symfony.md).


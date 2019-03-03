# Jumpgate App

- [Basic Installation](#basic-installation)
- [Users](#users)

<a name="basic-installation"></a>
## Basic Installation

```
cd <project dir>
git clone git@github.com:JumpGateio/JumpGate.git ./
composer install
php artisan jumpgate:setup
```
At this point, your site will display the JumpGate home page using bootstrap 4.  From here on out, you will customize as 
you normally would.

> You can run `php artisan jupmgate:css` to switch the front end to bootstrap 3 or uikit.

1. Set up your database in the `.env` file
1. Run `php artisan jumpgate:telescope`.
1. Run `php artisan migrate`.

<a name="users"></a>
## Users

If your site will need users you should modify the steps listed above.

```
cd <project dir>
git clone git@github.com:JumpGateio/JumpGate.git ./
composer install
php artisan jumpgate:setup --users --force
```

> `--force` is used to verify the users package can overwrite existing files that it published.

1. Set up your database in the `.env` file
1. Update your `config/jumpgate/users.php`.
    - If you enable social, remember to re-run `vendor:publish`.
1. Run `php artisan jumpgate:telescope`.
1. Run `php artisan jumpgate:user-database`

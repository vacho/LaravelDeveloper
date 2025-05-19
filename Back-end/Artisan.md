Artisan
===
The main commands.

```bash
# Command to run migrations.
php artisan migrate
# Restart the database structure and data.
php artisan migrate:refresh
# Restart the database structure and data and reload seedds.
php artisan migrate:refresh --seeds

# Generate a migration. (dabase table strcuture)
php artisan make:migration create_listings_table

# Generate a model (acces to database table)
php artisan make:model listing

```


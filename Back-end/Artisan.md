Artisan
===
The main commands.

```bash
# Command to run migrations.
php artisan migrate
# Restart the database structure and data.
php artisan migrate:refresh
# Install seed data.
php artisan migrate:refresh --seed
php artisan db:seed

# Generate a migration. (dabase table strcuture)
php artisan make:migration create_listings_table

# Generate a model (acces to database table)
php artisan make:model Listing

# Generate a factory
php artisan make:factory ListingFactory

# Generate a controller
php artisan make:controller ListingController

# Clear and recompile views
php artisan view:clear
php artisan cache:clear
php artisan config:clear
```


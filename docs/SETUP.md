# Local setup and known gaps

## Prerequisites

Use a local PHP environment with PDO MySQL enabled, MySQL, and a PHP-capable web server (for example Apache in a local development stack). GitHub Pages serves static files and cannot execute this PHP application.

## Restore the database

The repository contains no original SQL export. Recover the original `ecomm` schema and seed data before attempting a full run. Do not infer a complete schema from individual queries or assume default administrator accounts exist.

With a recovered export, create a local database and import it:

```bash
mysql -u YOUR_LOCAL_USER -p -e "CREATE DATABASE ecomm CHARACTER SET utf8mb4;"
mysql -u YOUR_LOCAL_USER -p ecomm < /path/to/recovered-ecomm.sql
```

These commands are templates. Choose a local account and confirm that the recovered schema supports the required tables and relationships.

## Configure and run

1. Edit `includes/conn.php` locally with the database host, database name and a dedicated local database account. Keep private credentials out of commits.
2. Serve the repository through your local PHP web server.
3. Open `index.php`; confirm product data loads without PDO errors.
4. Configure external CAPTCHA/email services before validating registration or email flows. Verify any payment-related integrations independently; the project's stated checkout scope is simulated.
5. Test user and admin workflows with sample data, including access control and image uploads.

## Reproducibility limits

No verified database dump, tested runtime version matrix or complete dependency lockfile is currently supplied. Bundled vendor files are retained for compatibility. Documentation does not certify a successful clean installation or production readiness.

## Next recovery step

Add a sanitized original database export with sample data and documented test accounts, then record PHP/MySQL versions and an end-to-end verification run. Remove personal customer data and credentials before publishing any export.


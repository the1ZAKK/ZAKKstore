# ZAKKstore

A PHP/MySQL e-commerce application developed as a 2025 Computer Science graduation project by Zakaria Brim.

## Features

- Product browsing and search across electronics and clothing.
- User accounts and shopping cart workflows.
- Simulated checkout and recorded sales.
- Administration of products, categories and users, with image uploads and sales summaries.

**Scope:** Academic demonstration. Checkout is described as simulated; this repository does not establish production-ready payments or security.

## Stack

PHP, MySQL, PDO, JavaScript, HTML/CSS and Bootstrap. Front-end and PHP libraries are bundled in the repository; retain their individual license notices.

## Setup status

**The original database export is missing from this repository.** The PDO connection expects an `ecomm` database. A clean clone cannot reproduce the full application until the original schema and seed data are recovered. See [setup instructions](docs/SETUP.md) for prerequisites, configuration and verification.

## Repository layout

- Root PHP pages: storefront, account, cart and transaction workflows.
- `includes/`: shared components, sessions and PDO connection.
- `admin/`: administration pages and supporting assets.
- Bundled assets and libraries: existing application dependencies.

## Validation checklist

After restoring the original database, verify product browsing/search, registration/login, cart changes, simulated checkout, recorded sales and admin access. Use local test accounts and sample data. External email, CAPTCHA and payment-related integrations need separate configuration and verification.

## Related work

[Portfolio case study](https://github.com/the1ZAKK/Portfolio/blob/main/portfolio-details-zakkstore.html)


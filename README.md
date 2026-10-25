# Balanceview org configuration

This repository holds **org-wide GitHub configuration** for all Balanceview
repositories. The public org profile is `profile/README.md`.

## Shared CI workflow templates

The `workflow-templates/` directory provides starter workflows that appear in
every repo under **Actions → New workflow → "By Balanceview"**:

| Template | What it does |
|----------|--------------|
| **Laravel CI (PHP 8.5 + MySQL)** | Installs deps, builds assets, runs `php artisan test` against a MySQL service. |
| **Laravel Lint (Pint)** | Checks PHP code style with `pint --test`. |

### How to use in a repo

1. Open the repo → **Actions** tab → **New workflow**.
2. Scroll to **"Workflows created by Balanceview"** and pick a template.
3. Commit it. It lands in `.github/workflows/` of that repo.

Each repo can customise the copied file (PHP version, branches, env) without
affecting the template.

> Note: these are *templates*, not org-enforced workflows. Org-required
> workflows + branch protection on private repos require a GitHub Team plan.

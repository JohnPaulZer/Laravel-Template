# Laravel Framework Template CLI tool

`laravel-template-jpz` is a CLI tool that creates a ready-to-use Laravel framework template.

Instead of manually creating the same Laravel folders, setup files, routes, assets, migrations, and tests every time you start a new project, you can run one command and get a clean application structure.

It generates a Laravel framework application with:

- Laravel 12
- Blade views
- Vite
- Tailwind CSS
- SQLite defaults
- API health-check route
- PHPUnit setup

This template is useful if you want to start a Laravel framework project quickly with a practical application skeleton already configured.

## What It Creates

The CLI creates a project with the usual Laravel folders:

- `app` - controllers, models, providers, and services
- `bootstrap` - Laravel application bootstrap files
- `config` - app, auth, cache, database, queue, mail, filesystems, logging, services, and session config
- `database` - SQLite database file, migrations, factories, and seeders
- `public` - front controller and public web assets
- `resources` - Blade views, CSS, and JavaScript
- `routes` - web, API, and console routes
- `storage` - local framework and log directories
- `tests` - feature and unit tests

It also includes a simple `/api/health` endpoint and a Blade home page so you can confirm the app is wired up.

## Quick Start

Create a new project folder:

```bash
npx laravel-template-jpz my-app
```

`my-app` is the name of the folder that will be created. You can replace it with any project name you want.

You can also run the CLI without a project name:

```bash
npx laravel-template-jpz
```

When you do not add a project name, the template files are created in the current folder.

If you created a new project folder, open it:

```bash
cd my-app
```

Install PHP dependencies:

```bash
composer install
```

Create the app key:

```bash
php artisan key:generate
```

Install and build frontend assets:

```bash
npm install
npm run build
```

Run migrations:

```bash
php artisan migrate
```

Start the development server:

```bash
composer run dev
```

The Laravel framework app will run at:

```text
http://localhost:8000
```

The health-check API route will be available at:

```text
http://localhost:8000/api/health
```

## Using Global Install

You can also install the CLI globally:

```bash
npm install -g laravel-template-jpz
```

The `-g` means global. This installs the CLI tool on your computer instead of inside one project folder.

After global installation, npm makes the `laravel-template-jpz` command available in your terminal. This means you can run the command from any folder without using `npx`.

Then create a project with:

```bash
laravel-template-jpz my-app
```

This command creates a new folder called `my-app` and adds the Laravel framework template files inside it.

## Command Format

```bash
npx laravel-template-jpz [project-name]
```

Examples:

```bash
npx laravel-template-jpz my-laravel-project
```

```bash
npx laravel-template-jpz
```

If you add a project name, the CLI creates a folder with that name and puts the template files inside it.

If you do not add a project name, the CLI creates the template in the folder where you run the command.

Use `npx` when you only want to run the CLI once. Use global install if you want the command available on your computer all the time.

## Generated Folder Structure

```text
app/
  Http/
    Controllers/
  Models/
  Providers/
  Services/
bootstrap/
config/
database/
  factories/
  migrations/
  seeders/
public/
resources/
  css/
  js/
  views/
routes/
storage/
tests/
```

## License

This project is licensed under the MIT License.

That means you can use, copy, modify, and share this CLI tool for personal or commercial projects.

See the full license here: [LICENSE](LICENSE).

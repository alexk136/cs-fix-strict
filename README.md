# PHP CS Fixer Configuration

This repository provides a configuration file for [PHP CS Fixer](https://github.com/PHP-CS-Fixer/PHP-CS-Fixer), a tool designed to automatically enforce PHP coding standards and fix code style issues.

## Installation

To use this configuration in your project:

1. Copy the `.php-cs-fixer.dist.php` file to the root of your project.
2. Install PHP CS Fixer via Composer:
   ```bash
   composer require friendsofphp/php-cs-fixer
   ```
3. Run PHP CS Fixer to apply the configuration:
   ```bash
   vendor/bin/php-cs-fixer fix
   ```

## Configuration Details

The `.php-cs-fixer.dist.php` configuration:
- Adheres to **PSR-12** and **Symfony** coding standards.
- Enforces modern PHP practices, such as:
  - Short array syntax (`[]` instead of `array()`).
  - Strict types declaration.
  - Arrow functions where applicable.
  - Ordered class elements and imports.
- Applies to the `src` and `tests` directories.
- Includes rules for clean code, such as removing superfluous PHPDoc tags and ensuring consistent spacing.
- For a complete list of rules, see the `.php-cs-fixer.dist.php` file.

## Usage

Copy file data to .php-cs-fixer.dist.php in you project root folder or run:
```bash
mv ../repo/php-cs-fixer.dist.php .php-cs-fixer.dist.php
```

Run PHP CS Fixer with the provided configuration:
```bash
vendor/bin/php-cs-fixer fix --config=.php-cs-fixer.dist.php
```

To check for issues without modifying files, use:
```bash
vendor/bin/php-cs-fixer fix --dry-run
```

## Contributing

Contributions are welcome! If you have suggestions for improving the configuration:
1. Fork this repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes and commit (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

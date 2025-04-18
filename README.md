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

## Comparison: Custom Config vs `@PER-CS2.0`

1. **Modern Best Practices**  
   Includes `declare_strict_types`, `use_arrow_functions`, `static_lambda`, `strict_comparison`, and `final_internal_class` — promoting clean, future-proof code.

2. **Refined Rule Selection**  
   You explicitly enable or disable rules like `class_definition`, `phpdoc_to_comment`, and `no_break_comment`, giving you full control rather than relying on blanket presets.

3. **Flexible `native_function_invocation`**  
   Unlike `@PER-CS2.0`, your config uses `strict: false`, allowing `use function` imports and preventing unwanted global backslashes.

4. **Improved Readability**  
   With fine-grained formatting control (`cast_spaces`, `trailing_comma_in_multiline`, `ordered_imports`, `concat_space`), the resulting code is more readable and consistent.

5. **Clean Class Structure**  
   The custom `ordered_class_elements` block ensures logical organization of class elements, which is often missing in default presets.

6. **Enhanced PHPUnit Style**  
   Enforcing `php_unit_construct` and `php_unit_method_casing` ensures consistent test structure without relying on broader, less focused test presets.

7. **Comment and Docblock Hygiene**  
   Your inclusion of `phpdoc_order`, `phpdoc_align`, and trimming rules improves the clarity of PHPDoc without over-relying on auto-removal.

8. **No Useless Code**  
   Rules like `no_useless_return` and `no_useless_else` keep the codebase minimal and expressive.

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

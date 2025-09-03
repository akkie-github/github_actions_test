# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a simple PHP project designed for testing GitHub Actions. The project contains basic PHP code with automated code formatting via GitHub Actions.

## Development Commands

### Code Formatting
- **Check formatting (dry-run)**: `./vendor/bin/php-cs-fixer fix --dry-run --diff --diff-format=udiff --using-cache=no .`
- **Apply formatting**: `./vendor/bin/php-cs-fixer fix --using-cache=no`

### Setup
The project uses PHP-CS-Fixer for code formatting. Install it via:
```bash
composer require --dev friendsofphp/php-cs-fixer
```

## Code Architecture

- **test.php**: Contains simple PHP logic for testing purposes
- **.php_cs.dist**: PHP-CS-Fixer configuration file with PSR2 standards, strict parameters, and short array syntax
- **GitHub Actions**: Automated workflow that runs PHP-CS-Fixer on every push and commits formatting changes back to the repository

## Formatting Rules

The project follows PSR2 coding standards with additional rules:
- `strict_param`: Enforces strict parameter declarations
- `array_syntax`: Uses short array syntax (`[]` instead of `array()`)
- Risky rules are allowed
- Vendor directory is excluded from formatting
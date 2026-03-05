# PHP CI Docker Images

Pre-built Docker images for running PHP test suites with SQLite in CI/CD pipelines. Available for multiple PHP versions.

## Purpose

These images are designed for PHP testing pipelines that use SQLite as the test database. They include all necessary PHP extensions and dependencies to run PHPUnit, Pest, or other PHP testing frameworks without requiring external database services.

## Available Versions

- `php8.3`

## What's Included

- **PHP CLI**
- **Composer**
- **SQLite Support**
- **Essential PHP Extensions**:
  - `pdo` & `pdo_sqlite` - Database support
  - `mbstring` - Multibyte string handling
  - `intl` - Internationalization
  - `gd` - Image processing
  - `zip` - Archive handling
  - `bcmath` - Arbitrary precision math
  - `pcntl` - Process control
  - `opcache` - Performance optimization

## Configuration

Images are pre-configured with optimized PHP settings for CI:
- Memory limit: 512M
- Max execution time: 300 seconds
- Opcache enabled

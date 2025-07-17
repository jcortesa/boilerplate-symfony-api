# PHP Event Booking API

[![PHP](https://img.shields.io/badge/PHP-8.3+-blue.svg)](https://www.php.net/) [![Symfony](https://img.shields.io/badge/Symfony-7.3+-black.svg)](https://symfony.com/) [![Docker](https://img.shields.io/badge/Docker-Compose-blue.svg)](https://docs.docker.com/compose/) [![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

## Table of Contents
- [Summary](#summary)
- [Requirements](#requirements)
- [Installation](#installation)
- [Unit Testing](#unit-testing)
- [Acceptance Testing](#acceptance-testing)
- [License](#license)

## Summary

A REST API in PHP for managing events and bookings. Applied good programming practices, SOLID/DRY principles and following hexagonal architecture.

The development process is based on Test Driven Development (TDD), starting with the API tests, which define the expected behavior of the API. Then, the API is developed to meet the expectations, mocking everything until implementation is complete.

## Requirements

- `Docker` and `Docker Compose` installed on your machine

## Installation

```sh
docker compose up --build
```

As an alternative, if [Make](https://www.gnu.org/software/make/manual/make.html) is installed, you can run:

```sh
make build
```

See available [Makefile targets](Makefile) for more options.

Now, on browser, you can access the REST API at [http://localhost:8000](http://localhost:8000).

## Testing

### REST API execution

Execute the API tests from `docs/api.http`. See the [HTTP Client documentation](https://www.jetbrains.com/help/phpstorm/http-client-in-product-code-editor.html) for more details on how to run these tests.

### Unit Testing

```sh
docker exec -it event-booking-api ./bin/phpunit
```

### Acceptance Testing

```sh
docker exec -it event-booking-api ./bin/phpunit --group=acceptance
```

## License

This project is licensed under the MIT License—see the [LICENSE](LICENSE) file for details.
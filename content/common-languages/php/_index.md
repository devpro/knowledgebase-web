---
title: "PHP"
date: 2019-09-20T11:42:08+02:00
draft: false
weight: 50
---

## Content

{{% children sort="Name" %}}

## Learn

### PHP on Windows

#### Nginx

#### CGI

- Create a bat file, for example start-php-fcgi.bat:

```bat
@ECHO OFF
ECHO Starting PHP FastCGI...
set PATH=D:\Programs\php-7.2.4-nts-Win32-VC15-x64;%PATH%
c:\bin\RunHiddenConsole.exe D:\Programs\php-7.2.4-nts-Win32-VC15-x64\php-cgi.exe -b 127.0.0.1:9123
```

### Tools

#### phpdbg

- [PHP RFC: phpdbg](https://wiki.php.net/rfc/phpdbg)
- [krakjoe/phpdbg](https://github.com/krakjoe/phpdbg)

### Unit tests

#### PHPUnit

[PHPUnit](https://phpunit.de/) is a testing framework for PHP. It is open source: [sebastianbergmann/phpunit](https://github.com/sebastianbergmann/phpunit). It is available on [packagist](https://packagist.org/packages/phpunit/phpunit).

##### Getting started with PHPUnit

- Read [Getting Started with PHPUnit 8](https://phpunit.de/getting-started/phpunit-8.html)

- Install locally: `composer require phpunit/phpunit --dev`
  - Check the tool is running file: `php vendor/phpunit/phpunit/phpunit --version` (or `php vendor/bin/phpunit` on a non-Windows environment)

- Edit `composer.json` file and execute `composer install` to regenerate autoload file

  ```json
  "autoload": {
      "psr-4": {
          "App\\": "src/"
      }
  },
  "autoload-dev": {
      "psr-4": {
          "App\\Tests\\": "tests/"
      }
  }
  ```

- Create `phpunit.xml.dist` file:

  ```xml
  <?xml version="1.0" encoding="UTF-8"?>
  <!-- https://phpunit.de/manual/current/en/appendixes.configuration.html -->
  <phpunit xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xsi:noNamespaceSchemaLocation="http://schema.phpunit.de/6.5/phpunit.xsd"
           backupGlobals="false"
           colors="true"
           bootstrap="config/bootstrap.php">
      <php>
          <ini name="error_reporting" value="-1" />
          <env name="APP_ENV" value="test" />
          <env name="SHELL_VERBOSITY" value="-1" />
      </php>
      <testsuites>
          <testsuite name="Project Test Suite">
              <directory>tests</directory>
          </testsuite>
      </testsuites>
      <filter>
          <whitelist>
              <directory>src</directory>
          </whitelist>
      </filter>
  </phpunit>
  ```

- Launch the tests: `php vendor/phpunit/phpunit/phpunit -c phpunit.xml.dist --log-junit junit.xml`
  - With coverage ([Code Coverage Analysis](https://phpunit.readthedocs.io/en/8.0/code-coverage-analysis.html)): `php vendor/phpunit/phpunit/phpunit -c phpunit.xml.dist --coverage-html .build/coverage-report --coverage-clover .build/coverage.xml`
  - Integration in SonarCloud: [PHP Unit Tests and Coverage Results Import](https://docs.sonarqube.org/display/PLUG/PHP+Unit+Tests+and+Coverage+Results+Import)

- We can also use **phpdbg** (that is now shipped with PHP): `phpdbg -qrr vendor/phpunit/phpunit/phpunit -c phpunit.xml.dist` (comparison with xdebug here: [Generating Code Coverage with PHPUnit and phpdbg](https://hackernoon.com/generating-code-coverage-with-phpunite-and-phpdbg-4d20347ffb45))

- You can also use Symfony PHPUnit bridge: `composer install symfony/phpunit-bridge --dev` (and create a bin/console and update your gitignore)

- For Mocks : [Test Doubles](https://phpunit.readthedocs.io/en/8.0/test-doubles.html)

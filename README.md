# Redmine Locale Float Format

A small [Redmine](https://www.redmine.org/) plugin that lets users enter and see float custom fields with the decimal separator of their language.

## Introduction

Redmine offers almost everything we need out of the box. We only had to extend it a little for our internal needs, and this plugin was the result.

## Features

Redmine always uses a dot as decimal separator for float custom fields, regardless of the user's language. With this plugin, the separator and thousands delimiter defined in the locale (`number.format.separator` and `number.format.delimiter`) are used instead, e.g. `1.234,50` in German or `1,234.50` in English.

**Without plugin:**

![Example float field without plugin](screenshots/example-float-without-plugin.png)

**With plugin:**

![Example float field with plugin](screenshots/example-float-with-plugin.png)

The locale format is supported in:

- display of float values (shown with two decimal places)
- input fields of float custom fields, including bulk edit
- query filters on float custom fields
- copying issues and projects

Values are still stored in Redmine's standard format, so existing data stays untouched.

## Installation

1. Clone the plugin into the `plugins` directory of your Redmine installation. The directory name must be `locale_float_format`, as it has to match the plugin ID:

   ```bash
   cd /path/to/redmine/plugins
   git clone https://github.com/ablida/locale_float_format.git
   ```

   Alternatively, download the repository as a ZIP and extract it to `plugins/locale_float_format`.

2. Restart Redmine.

No database migrations are required. More information on installing Redmine plugins: [Redmine Plugins](https://www.redmine.org/projects/redmine/wiki/Plugins).

## Usage

No configuration is needed. After the restart, float custom fields use the format of each user's language.

## Uninstallation

Remove the `plugins/locale_float_format` directory and restart Redmine.

## License

This plugin is licensed under the [GNU General Public License v2.0](LICENSE), unless otherwise stated.

## About

Copyright (c) 2021–2026 ablida

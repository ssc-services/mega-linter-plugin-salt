# mega-linter-plugin-salt

This is a linter plugin for the excellent [MegaLinter](https://oxsecurity.github.io/megalinter), checks Salt State files (SLS) for best practices and behavior that could potentially be improved.

## Usage

To enable this plugin into your Megalinter config, add the following in your `.mega-linter.yml`:

```yaml
PLUGINS:
  - https://raw.githubusercontent.com/ssc-services/mega-linter-plugin-salt/main/mega-linter-plugin-salt/salt.megalinter-descriptor.yml
ENABLE_LINTERS:
  - SALT_SALTLINT
```

By default, the plugin will scan all `*.sls` file on your project, which might be broader than you'd like, so you may want to tweak the file selection options using the usual parameters, including:

- `SALT_DIRECTORY`
- `SALT_SALTLINT_FILTER_REGEX_INCLUDE`
- `SALT_SALTLINT_FILTER_REGEX_EXCLUDE`
- `SALT_SALTLINT_FILE_EXTENSIONS`
- `SALT_SALTLINT_FILE_NAMES_REGEX`

For further information have look at the Documentation of [MegaLinter](https://megalinter.io/latest/).

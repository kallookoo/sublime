# sublime

sublime is the parser for creating WordPress completions, use [WordPress PHPDoc Parser](https://github.com/WordPress/phpdoc-parser)

## Requirements
* PHP 5.6+
* [Composer](https://getcomposer.org/)
* [WP CLI](http://wp-cli.org/)

Clone the repository into your WordPress plugins directory:

```bash
git clone https://github.com/kallookoo/sublime.git
```

After that install the dependencies using composer in the parser directory:

```bash
composer install
```

## Running

In your site's directory

* Create or update import:

```bash
wp subl create /path/to/source/code --user=<id|login>
```

* Create or update completions:

```bash
wp subl generate --directory=/path/to/export --type=<all|constants|capabilities|functions|hooks|actions|filters|classes>
```

# Notes

* Use files inside to `sublime/config/` folder for change defaults filters. Optional
* Use folder `sublime/missing` for include missing, by default if defined constants.php for include by example WP_HOME constant, this plugin auto load all files inside this folder on import
* The vagrant folder contains files for personal use, they are used to streamline processes.
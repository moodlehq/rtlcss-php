RTLCSS for PHP
--------------

RTLCSS is a framework for converting Left-To-Right (LTR) Cascading Style Sheets(CSS) to Right-To-Left (RTL).

## Usage

### Installation using composer

Add the library to your composer.json

```json
{
    "repositories": [{
        "type": "vcs",
        "url": "https://github.com/moodlehq/rtlcss-php"
    }],
    "require-dev": {
        "moodlehq/rtlcss-php": "*"
    }
}
```

### Flipping

```php
$tree = new Sabberworm\CSS\Parser($css);
$rtlcss = new MoodleHQ\RTLCSS\RTLCSS($tree);
$rtlcss->flip();
echo $tree->render();
```

For parsing options and rendering, refer to [Sabeerword/PHP-CSS-Parser](https://github.com/sabberworm/PHP-CSS-Parser).

## About this tool

This tool is very heavily inspired by [MohammaYounes/rtlcss](https://github.com/MohammadYounes/rtlcss), even though at this stage it does not include all of its features. See this library as a partial port of the latter.

## License

Licensed under the [GNU GPL License](http://www.gnu.org/copyleft/gpl.html).

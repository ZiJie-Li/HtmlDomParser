# SimpleHtmlDomParser
Add library Simple html dom to Laravel
More document: [http://simplehtmldom.sourceforge.net/](http://simplehtmldom.sourceforge.net/)

##How to install
```
composer require royalmar/simple-html-dom-parser
```

##Laravel Setup
Add the service provider to config/app.php:
```
'providers' => array(
    ...
    'Royalmar\HtmlDomParser\HtmlDomParserServiceProvider',

    //Laravel 5.1+
    Royalmar\HtmlDomParser\HtmlDomParserServiceProvider::class,
    ...
```

Add alias to config/app.php:
```
'aliases' => array( 
    ...
    'HtmlDomParser' => 'Royalmar\HtmlDomParser\HtmlDomParser',

    //Laravel 5.1+
    'HtmlDomParser' => Royalmar\HtmlDomParser\HtmlDomParser::class,
    ...
```

##Usage
```php
$parser = new \HtmlDomParser();
// get html dom from file
$html = $parser->fileGetHtml('http://www.google.com');
// get html dom from string
$html = $parser->strGetHtml('<p>Hello World</p>');

//OR

// get html dom from file
$html = \HtmlDomParser::fileGetHtml('http://www.google.com');
// get html dom from string
$html = \HtmlDomParser::strGetHtml('<p>Hello World</p>');
```

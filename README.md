Translate CSS selectors to XPath queries.
=========================================

A lightweight and dependency free CSS to XPath translator.

***

<a href="https://circleci.com/gh/PhpGt/CssXPath" target="_blank">
	<img src="https://badge.status.php.gt/cssxpath-build.svg" alt="Build status" />
</a>
<a href="https://scrutinizer-ci.com/g/PhpGt/CssXPath" target="_blank">
	<img src="https://badge.status.php.gt/cssxpath-quality.svg" alt="Code quality" />
</a>
<a href="https://scrutinizer-ci.com/g/PhpGt/CssXPath" target="_blank">
	<img src="https://badge.status.php.gt/cssxpath-coverage.svg" alt="Code coverage" />
</a>
<a href="https://packagist.org/packages/PhpGt/CssXPath" target="_blank">
	<img src="https://badge.status.php.gt/cssxpath-version.svg" alt="Current version" />
</a>
<a href="http://www.php.gt/dom" target="_blank">
	<img src="https://badge.status.php.gt/cssxpath-docs.svg" alt="PHP.Gt/CssXPath documentation" />
</a>

Example usage
-------------


```php
$html = <<<HTML
<form>
	<label>
		Name
		<input name="name" />
	</label>
	<label>
		Code:
		<input name="code" />
	</label>
	<button name="do" value="submit">Submit code</button>
</form>
HTML;

$document = new DOMDocument();
$document->loadHTML($html);

$xpath = new DOMXPath($document);
$inputElementList = $xpath->query(new Translator("form>label>input");
```

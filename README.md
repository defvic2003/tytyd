<?php

use Herrera\FileLocator\Locator\FileSystemLocator;

$locator = new FileSystemLocator('/path/to/dir');
$locator = new FileSystemLocator(array(
    '/path/to/dir1',
    '/path/to/dir2',
    '/path/to/dir3' // etc
));

$file = $locator->locate('file.ini'); // return the first "file.ini" found
$files = $locator->locate('file.ini', false); // find all named "file.ini"

#service

# PHAR Files
## What is PHAR Files?
PHP Archive files are compiled PHP libraries, similar to DLLs.

## Any documentation on PHAR Files?
TODO

## How do I run code on PHAR Files?
* include the PHAR file in a PHP file
* access it directly - writing `<?php` tags in a PHAR file will cause a webserver to render it. Use that if you find an LFI and you can't upload a PHP file.
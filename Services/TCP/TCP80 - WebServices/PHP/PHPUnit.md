#service

# PHPUnit
## What is PHPUnit?
PHPUnit is a unit testing framework for the PHP programming language.

## How do I connect to PHPUnit?
TODO Web browser.

## Any documentation on PHPUnit?
TODO Look up PHPUnit

## How do I collect info from PHPUnit?
TODO

## How do I run code on PHPUnit?
### CVE-2017-9841
PHPUnit has an unauthenticated RCE vulnerability in versions before 5.6.3, where using a POST request to the file `eval-stdin.php` with valid php code can result in shell command execution.
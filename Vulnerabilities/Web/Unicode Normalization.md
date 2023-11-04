#vulnerability

# Unicode Normalization
## What is Unicode Normalization?
Unicode Normalization is a process software uses to break down complex Unicode characters into simple ASCII ones. This can give you...

## What does Unicode Normalization give me?
* Filter bypass - they never expect a two-byte `..` character.
* Path Traversal!
* OS Command injection
* many cool things

## Any documentation on Unicode Normalization?
[Lazarv - Unicode Normalization](https://lazarv.com/posts/unicode-normalization-vulnerabilities/)

## How do I verify that a target is vulnerable?
* Try some payloads!
* maybe patch DotDotPwn to include those!

## How do I use Unicode Normalization?
Look at documentation, but essentially just spam complex unicode chars that can be normalized to what you want!
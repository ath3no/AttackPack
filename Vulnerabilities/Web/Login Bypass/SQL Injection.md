#vulnerability

# SQL Injection
## What is SQL Injection?
Inject SQL queries to where they shouldn't be allowed. simple as that.

## What does SQL Injection give me?
Access to databases. Cool!

## Any documentation on SQL Injection?
Lots of places online.

## How do I verify that a target is vulnerable?
drop a '," and see what happens
or use `sqlmap`

## How do I use SQL Injection?
Find an SQLi cheat sheet and run with it, here are some common ones:
`' OR 1=1; --`
`' OR 1=1; #`
`" OR 1=1; --`
`" OR 1=1; #`
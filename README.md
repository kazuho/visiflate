visiflate
=========

dumps the internal state of the Deflate expander; useful for visualizing the algorithm

Usage
-----

```
% make
% gzip < alice.txt > alice.txt.gz
% ./puff -10 alice.txt.gz
puff() succeeded uncompressing 1328 bytes
8 compressed bytes unused
inpos=406,inbits=224,outpos=0,outbytes=45
    41 6c 69 63 65 20 77 61 73 20 62 65 67 69 6e 6e 69 6e 67 20 74 6f 20 67 65 74 20 76 65 72 79 20 74 69 72 65 64 20 6f 66 20 73 69 74 74
    A  l  i  c  e     w  a  s     b  e  g  i  n  n  i  n  g     t  o     g  e  t     v  e  r  y     t  i  r  e  d     o  f     s  i  t  t 

inpos=630,inbits=13,outpos=45,outbytes=4,distance=-29
    69 6e 67 20
    i  n  g    

inpos=643,inbits=32,outpos=49,outbytes=6
    62 79 20 68 65 72
    b  y     h  e  r 

inpos=675,inbits=11,outpos=55,outbytes=3,distance=-15
    20 73 69
       s  i 

inpos=686,inbits=9,outpos=58,outbytes=2
    73 74
    s  t 

inpos=695,inbits=11,outpos=60,outbytes=3,distance=-7
    65 72 20
    e  r    

inpos=706,inbits=72,outpos=63,outbytes=15
    6f 6e 20 74 68 65 20 62 61 6e 6b 2c 20 61 6e
    o  n     t  h  e     b  a  n  k  ,     a  n 

inpos=778,inbits=13,outpos=78,outbytes=5,distance=-42
    64 20 6f 66 20
    d     o  f    
```

Note: ```inpos``` represents the input position in bits, whereas ```outpos``` represents the output position in bytes.

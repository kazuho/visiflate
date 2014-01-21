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
i_pos   i_bits  o_pos   o_bytes dist    data
404     224     0       45              Alice was beginning to get very tired of sitt
628     12      45      4       -29     ing 
640     30      49      6               by her
670     11      55      3       -15      si
681     9       58      2               st
690     10      60      3       -7      er 
700     71      63      15              on the bank, an
771     13      78      5       -42     d of 
784     17      83      3               hav
801     12      86      4       -41     ing 
813     19      90      4               noth
832     15      94      7       -78     ing to 
847     19      101     3               do:
```

* i_pos   - input offset (in bits)
* i_bits  - bits used in input
* o_pos   - output offset (in bytes)
* o_bytes - number of output bytes
* dist    - distance of the text to be copied from (or none if not copied)
* data    - corresponding data

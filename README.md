visiflate
=========

dumps the internal state of the Deflate expander; useful for visualizing the algorithm

Usage
-----

```
% make
% gzip < puff.c > puff.c.gz
% ./puff -10 puff.c.gz
i_pos   i_bits  o_pos   o_bytes mode
583     9       0       1       direct
592     9       1       1       direct
601     9       2       1       direct
610     5       3       1       direct
615     9       4       1       direct
624     5       5       1       direct
629     7       6       1       direct
636     7       7       1       direct
643     7       8       1       direct
650     7       9       1       direct
657     8       10      1       direct
665     7       11      1       direct
672     14      12      4       copy
686     9       16      1       direct
(snip)
90088   19      38079   9       copy
90107   8       38088   1       direct
90115   18      38089   9       copy
90133   20      38098   10      copy
90153   18      38108   10      copy
90171   13      38118   5       copy
90184   6       38123   1       direct
90190   20      38124   10      copy
90210   25      38134   13      copy
90235   17      38147   4       copy
90252   18      38151   3       copy
puff() succeeded uncompressing 38154 bytes
8 compressed bytes unused
```

* i_pos   - input offset (in bits)
* i_bits  - bits used in input
* o_pos   - output offset (in bytes)
* o_bytes - number of output bytes
* mode    - direct / copy / stored

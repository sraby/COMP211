Editor I

Files you won't modify:
   gapbuf-test.c0 - For testing gap buffers interactively

Files you will modify:
   gapbuf.c0 - Gap buffers

==========================================================

Testing in coin
   % coin -d gapbuf.c0
   --> test_is_gapbuf();
   You can also write tests for other functions if you wish.  

Compiling and running testing gapbuf:
   % cc0 -d -o gapbuf-test gapbuf.c0 gapbuf-test.c0
   % ./gapbuf-test
   Visualizing the 16-element gap-buffer.
   Give initial input (empty line quits):
   space race<<<<<<<<^p<<the >>^p>>>>>>>>!!<<<<<<<^^^^^great
        [................]
   's': s[...............]
   'p': sp[..............]
   'a': spa[.............]
   ...

==========================================================

Submitting:
    Copy the file gapbuf.c0 to your handin directory on WesFiles.  

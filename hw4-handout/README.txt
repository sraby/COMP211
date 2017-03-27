Programming 3 (Twitter)

Files you won't modify:
   lib/arrayutil.c0     - Array spec functions
   lib/readfile.c0      - File reading library 
   lib/stringsearch.c0  - String searching library
   lib/selectionsort.c0 - String sorting library 

Files that you will modify:
   duplicates.c0        - Code for part 1
   count.c0             - Code for part 2

Data:
   texts/vocab_sorted.txt 
   texts/vocab_sorted_small.txt 
   texts/twitter_1.txt
   texts/twitter_1k.txt
   texts/twitter_200k.txt

   You can create more data files if you would like to use them in
   your tests: just hand these in along with your other files.

==========================================================

Loading duplicates.c0 in coin to test it.
   % coin -d lib/*.c0 duplicates.c0
   --> test_duplicates();

Compiling count.c0 for testing (contract checking enabled):
   % cc0 -d -o count-debug lib/*.c0 duplicates.c0 count.c0 count-main.c0

    OR

   % make debug
   
  THEN to run it, do 

   % ./count-debug -v texts/vocab_sorted_small.txt -t texts/twitter_1k.txt -f fast -top 10

Compiling count.c0 for performace (contract checking disabled):
   % cc0 -o count lib/*.c0 duplicates.c0 count.c0 count-main.c0

   OR

   % make
   
 THEN to run it, do 

   % ./count -v texts/vocab_sorted.txt -t texts/twitter_200k.txt -f fast -top 10


Explanation of count/count-debug options

   -v <vocab_file> specifies the words whose frequencies are counted.  Choices are
      texts/vocab_sorted.txt
      texts/vocab_sorted_small.txt

   -t <twitter_file> specifies the tweets to count.  Choices are
      texts/twitter_200k.txt
      texts/twitter_1k.txt
      texts/twitter_1.txt

   -f <speed> specifies linear/binary search.  Choices are
      fast
      slow

   -top <num> [OPTIONAL] specifies to print the <num> most frequent tweets


Examples:

   % ./count -v texts/vocab_sorted.txt -t texts/twitter_200k.txt -f fast -top 10
   Run with contracts off,
       on full vocab list, with 200k tweets, binary search, and print top 10

   % ./count -v texts/vocab_sorted.txt -t texts/twitter_200k.txt -f fast
   Run with contracts off,
       on full vocab list, with 200k tweets, binary search; don't print anything

   % ./count-debug -v texts/vocab_sorted_small.txt -t texts/twitter_1.txt -f slow -top 10
   Run with contracts on, 
       on small vocab list, with 1 tweet, linear search, and print top 10

==========================================================

To hand in the assignment, copy count.c0 and duplicates.c0 to your
handin directory on WesFiles.  

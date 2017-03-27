Doubly Linked Lists

Files you won't modify:
   is_dll_pt-test.c0 - Test is_dll_pt
   dll_pt-test.c0 - Test for doubly-linked lists with a point
   elem_char.c0 - Defines dll element type to be char

Files you will modify:
   dll_pt.c0 - Doubly-linked lists with a point

==========================================================

Compiling and testing is_dll_pt:
   $ cc0 -d -o is_dll_pt-test elem-char.c0 dll_pt.c0 is_dll_pt-test.c0
   $ ./is_dll_pt-test

Compiling and testing dll_pt:
   $ cc0 -d -o run-dll elem-char.c0 dll_pt.c0 dll_pt-test.c0
   $ ./run-dll

Testing in coin
   $ coin -d elem-char.c0 dll_pt.c0 function-tests.c0
   --> Test_dll();
 
==========================================================

Submitting:
  
  Copy the file dll_pt.c0 to your handin directory on WesFiles

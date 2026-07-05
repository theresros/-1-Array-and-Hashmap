# -1-Array-and-Hashmap
Learn array and hash map in an interesting way
ARRAY

ex:an array is one unbroken block of memory, and every element lives at a predictable address.

1)insertion and deleting is difficult
 
 Now the interesting question: why is inserting in the middle of an array slow? Because if you want to insert a new house between arr[2] and arr[3], you can't just squeeze it in — the street would break. Every house from arr[3] onward has to physically shift over by one to make room. That's why insert/delete at an arbitrary index is O(n), while insert/delete at the end is O(1) — you're just building the next house on empty land.

 2)std::vector
 A vector doesn't ask for more land every single time you push_back — that would mean rebuilding the whole street constantly.

 3)

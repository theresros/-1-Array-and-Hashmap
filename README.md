# -1-Array-and-Hashmap
Learn array and hash map in an interesting way
ARRAY

ex:an array is one unbroken block of memory, and every element lives at a predictable address.

1)insertion and deleting is difficult
 
 Now the interesting question: why is inserting in the middle of an array slow? Because if you want to insert a new house between arr[2] and arr[3], you can't just squeeze it in — the street would break. Every house from arr[3] onward has to physically shift over by one to make room. That's why insert/delete at an arbitrary index is O(n), while insert/delete at the end is O(1) — you're just building the next house on empty land.

 2)std::vector
 A vector doesn't ask for more land every single time you push_back — that would mean rebuilding the whole street constantly.

 3)Hashing
 
No searching — the formula told you exactly where to go, the same way base + index told the array where to go. That formula is the hash function, and it's the entire reason lookups can be O(1) even though the key is a string, not a clean integer.

chaining i hashing
See what happened to "amy" and "kim" — they both landed in bucket 1. The map's answer is: don't fight it, just stack them. Bucket 1 now holds a tiny linked list of both entries (this strategy is called chaining, and it's what unordered_map uses under the hood). When you later look up "amy", the map hashes it, jumps straight to bucket 1, then does a quick walk through that short chain to find the exact match.

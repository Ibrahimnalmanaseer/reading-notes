# Hashtabels

## What Is a Hash Table?

Hash Table in Python utilizes an array as a medium of storage and uses the hash method to create an index where an element is to be searched from or needs to be inserted.

In other words, a Hash Table in Python is a data structure which stores data by using a pair of values and keys.

## Hash Functions

Hash means to cut, scramble, or chop something.
Following are some hash functions examples:
- To prevent sensitive data, such as web analytics, passwords, and payment details.
- To encrypt information exchange between browsers and web servers, and create session IDs for data caching and internet applications.
- To find identical data through lookup functions.
- Adding a digital signature to an email.


## Writing Hash Function

Division Method
If the size of the hash table is l and the indices to be found are those of key m, then the hash function is calculated as follows:

h(m) = m mod l

If hash size of the hash table is 10 and m=111 then h(m) = 111 mod 10 = 1, then the table size should never be in the powers of 2, as the binary form of the powers of 2, which is 2,4, 8 leads to 10, 100… and so on.

Multiplication Method
To find keys’ indices, the following hash function is followed:

h(m) = {l(A mod 1)}

where, 0<A<1 and 

(mA mod 1) gives the fractional part mA, and {} calculates the floor value.

Universal Hashing
The hash function is selected in a haphazard manner, independent of keys.

Hash Collision Sample
class City(str):

    def __hash__(self):

        return ord(self[0])

We generate a dictionary where the arbitrary values are allocated to cities

data =  {

    City("Venice"): 'Italy',

    City("Manchester"): 'UK',

    City("London"): 'UK',

    City("Madrid"): 'Spain',

}

"""

hash("Madrid") = ord("M") & 0b111

                  = 66 & 0b111

                  = 0b1000010 & 0b111

                  = 0b010 = 2

hash("Venice") = ord("R") & 0b111

             = 82 & 0b111

             = 0b1010010 & 0b111

             = 0b010 = 2

"""

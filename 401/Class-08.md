# LinkedList

## Data Structures

A data structure is a specialized format for organizing, processing, retrieving and storing data,Data structures make it easy for users to access and work with the data they need in appropriate ways.

### Five factors to consider when picking a data structure:

- What kind of information will be stored?
- How will that information be used?
- Where should data persist, or be kept, after it is created?![linked_list_insertion_2](https://user-images.githubusercontent.com/62019258/196277755-06248c96-5563-4c10-abfd-f0d1326af572.jpg)

- What is the best way to organize the data?
- What aspects of memory and storage reservation management should be considered?


#### Some examples of how data structures are used include the following:

- **Storing data** Data structures are used for efficient data persistence, such as specifying the collection of attributes and corresponding structures used to store records in a database management system.
- **Ordering and sorting** Data structures such as binary search trees -- also known as an ordered or sorted binary tree -- provide efficient methods of sorting objects, such as character strings used as tags. With data structures such as priority queues, programmers can manage items organized according to a specific priority.
- **Indexing.** Even more sophisticated data structures such as B-trees are used to index objects, such as those stored in a database.
- **Searching.** Indexes created using binary search trees, B-trees or hash tables speed the ability to find a specific sought-after item.
- **Scalability.** Big data applications use data structures for allocating and managing data storage across distributed storage locations, ensuring scalability and performance. Certain big data programming environments -- such as Apache Spark -- provide data structures that mirror the underlying structure of database records to simplify querying.

#### Characteristics of data structures:

Data structures are often classified by their characteristics :

- **Linear or non-linear.** This characteristic describes whether the data items are arranged in sequential order, such as with an array, or in an unordered sequence, such as with a graph.
- **Homogeneous or heterogeneous**. This characteristic describes whether all data items in a given repository are of the same type. One example is a collection of elements in an array, or of various types, such as an abstract data type defined as a structure in C or a class specification in Java.
- **Static or dynamic.** This characteristic describes how the data structures are compiled. Static data structures have fixed sizes, structures and memory locations at compile time. Dynamic data structures have sizes, structures and memory locations that can shrink or expand, depending on the use.



#### Data types :

- **Boolean**
- **integer**
- **Floating-point numbers**
- **Fixed-point numbers**
- **Character**
- **Pointers**
- **String**


#### Types of data structures :

- **Array.**
- **Stack.**
- **Queue**
- **Linked list:** A linked list stores a collection of items in a linear order. Each element, or node, in a linked list contains a data item, as well as a reference, or link, to the next item in the list.
- **Tree**
- **Heap**
- **Graph.**
- **Trie.**
- **Hash table.**

- - - -

## Data Structure and Algorithms - Linked List

Linked List is a sequence of links which contains items. Each link contains a connection to another link.

- **Link**: Each link of a linked list can store a data called an element.

- **Next**: Each link of a linked list contains a link to the next link called Next.

- **LinkedList**: A Linked List contains the connection link to the first link called First.

![linked_list](https://user-images.githubusercontent.com/62019258/196276281-397a1106-66b8-49e6-9786-7037ea7a15fc.jpg)

### Basic Operations

- **Insertion Operation**:


![linked_list_insertion_0](https://user-images.githubusercontent.com/62019258/196277218-c546325c-2ff3-4a09-ae6d-b7fbc04962b2.jpg)


``` NewNode.next −> RightNode; ```

![linked_list_insertion_1](https://user-images.githubusercontent.com/62019258/196277358-15ee38f8-a648-4e1a-8e91-2b30a886c031.jpg)

``` LeftNode.next −> NewNode; ```


![linked_list_insertion_3](https://user-images.githubusercontent.com/62019258/196277785-7aaece93-d761-4229-97c4-5109e306a50e.jpg)



- **Deletion Operation**:

``` LeftNode.next −> TargetNode.next; ```

![linked_list_deletion_1](https://user-images.githubusercontent.com/62019258/196277955-0de8a9dc-2312-47e8-8db1-427b2fa2a184.jpg)


``` TargetNode.next −> NULL; ```

![linked_list_deletion_2](https://user-images.githubusercontent.com/62019258/196278020-7a8c2002-9c71-43ca-87bd-89b807237eee.jpg)



![linked_list_deletion_3](https://user-images.githubusercontent.com/62019258/196278247-2c49c406-7b8e-4595-b8c0-f80abaf05237.jpg)



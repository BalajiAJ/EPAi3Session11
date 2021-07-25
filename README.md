# Session 11 Assignment on Iterable and Iterator

### An iterable is any Python object capable of returning its members one at a time, permitting it to be iterated over


Iterator in python is an object that is used to iterate over iterable objects like lists, tuples, dicts, and sets. The iterator object is initialized using the iter() method. It uses the next() method for iteration.
 
### __iter__(iterable)__ method that is called for the initialization of an iterator. This returns an iterator object
### __next__  -  The next method returns the next value for the iterable. When we use a for loop to traverse any iterable object, internally it uses the iter() method to get an iterator object which further uses next() method to iterate over. This method raises a StopIteration to signal the end of the iteration.

How an iterator really works in python is demosntrated in the below example:

Here we have two classes Polygon and Polygons written in session11.py and polysequence.py

##Iterable
Here polysequence returns a list of polygons starting from edges of 3 to the value passed in the constructor. This custom polygons is a list which is also an iterable.

This Polygons iterable which means we can get individual item from the iterable, we can get the length of the ietrable and parse through individual items using for loop. when using an iterable all the values will be stored in the memory

The Polygons class has __iter__, __len__,__getitem__ methods to perform above operations.

##Iterator
So, here we are creating a sub class IteratorPolygon that is used as an iterator on top of Polygons iterable.

The advantage of iterator is the ability to use next to parse through each and every items in the list. There by we are storing only those individual item in the memory.

The iterator implements __next__ and __iter__ methods.

Once the iterator passed through the last item in the the iterable, it will give a stopiteration error




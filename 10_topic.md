---
layout: page
title: Main topic
---

## Matrices and matrix objects in GAP


Originally, matrices in GAP where introduced  as lists of lists of equal
length with entries in a (usually common) ring. Advantages of this setup
are simplicity and flexibility.

But there are also disadvantages, for example:

 - it can be expensive to find out if a GAP object is a matrix
 - it  is easy  to  fall  into efficiency  traps  related  to GAPs  type
   determination of nested lists
 - one cannot store  meta-information about a matrix in a  list of lists
   (e.g., a ground ring, or various properties and attributes)
 - it  is difficult  to  make  functions for  matrices  work with  other
   matrices which  are not implemented  as lists of lists  (e.g., sparse
   matrices, wrapped matrices from external programs)
 - matrices  with zero  rows or  columns do  not work  well (useful  for
   programming, an  empty list  has no information  about which  type of
   elements it does not contain)

There exists plans, descriptions and code for *matrix objects* in the 
GAP library. Goals of this meeting could be:

 - to clearify open points in the usage interface (API) of such objects
 - to document this API
 - to implement  (or finish  partial implementations)  of some  types of
   matrices according to the API
 - to make as much code as possible  in the GAP library work with matrix
   objects instead of list-of-lists matrices  (e.g., the creation of and
   computation with matrix  groups where generators are  given as matrix
   objects)

A more detailed account of the current status was given by Max Horn in
[this github issue](https://github.com/gap-system/gap/issues/945).



---
description: ""
title: "Haskell language reference"
draft: false
weight: 200
bref:
toc: true
---

# applicatives
- monads were added before applicative
- applicative is a superclass of monad
- inspired by a paper - http://strictlypositive.org/Idiom.pdf
- applicative has a bunch of laws (in category theory)
- if something implements applicative it should follow these laws
- it is possible to implement without the laws but it isn't a valid instance
- none of the laws are checked by the type system but we can check them with tests (ie property tests)

Brian: Functor -> Monoid -> Monad https://www.youtube.com/watch?v=ZhuHCtR3xq8
Relationship: Applicative-Monoid https://www.youtube.com/watch?v=RtYWKG_zZrM

- http://adit.io/posts/2013-04-17-functors,_applicatives,_and_monads_in_pictures.html (use pictures but descriptions about wrapping are incorrect/needs better descriptive language)

# datatype


# functor
Representation of the mathematical functor: a mapping between categories in the context of category theory.

- https://wiki.haskell.org/Functor

# fold
A fold deals with two things: a combining function, and a data structure, typically a list of elements. The fold then proceeds to combine elements of the data structure using the function in some systematic way. 

- https://wiki.haskell.org/Fold
- https://wiki.haskell.org/Foldr_Foldl_Foldl'

# hask
In terms of category theory, Hask is the category of Haskell types and functions. The objects of Hask are Haskell types.

- https://wiki.haskell.org/Hask

# lens
- https://github.com/ekmett/lens/wiki/Derivation

# type

# string
String has exactly one use, and that’s showing Hello World in tutorials. For all other uses it is the wrong choice and you should instead you should use Text for encoded textual strings and ByteString if you are dealing with raw bites in memory.

The default String type in Haskell is defined as type String = [Char], meaning a String is a list of characters. It has nothing to say about encodings, efficiency of storage (that list is going to be a linked list under the hood) or anything really that you would expect from a modern language. 

# newtype
- cannot be a sumtype
- needs to have a constructor which can only take in a singular argument

# acknowledgements
- Uses content from https://wiki.haskell.org/HaskellWiki:Copyrights

ipa
===

A database for IPA plus a simple web interface.
--------------------

Try it at http://wugbot.org/ipa/

This repo has a couple goals:

1. to serve as a source for a lightweight database the data encoded into the International Phonetic Alphabet. Current target formats are JSON and CSV.
2. to serve as the basis for an orthography/IPA conversion library.

(2) is harder, and will probably end up being its own project. Here's the use case:

Suppose you're interested in two or more variants of the same language family. Let's say (this happens to be the case in my own work) variants of Mixteco Bajo.  There are extant sources on these variants, but they happen to be written in different orthographies, even for the _same_ variant (linguist 1 made up her up, linguist 2 made up another…). So you might have materials on Variant A where low tone is written «à», whereas in Variant B it’s written «a̱». Or maybe a voiced bilabial fricative is written «β» or «v»… etc, etc. 

Now, let’s imagine you have two lexicons, one in A and one in B. You know that there is a word «vìlú» which means ‘cat’ in A, and you want to search for whatever means ‘cat’ in some _texts_ (not a lexicon!) of B. Which means you need to search for «βiru» because let’s say the orthography of B uses «β» instead of «v», and blah blah blah.

Anyway, you see what I mean. What you really want to be able to do is do string similarity on the _phonetic_ representation, not the _orthographic_ representation. This boils down to saying that it should be possible to convert between orthographic and phonetic (or phonological) representations of the same linguistic content. (Yes, there are tricky edge cases. But they are edge cases! And string similarity can be fuzzed out over those edge cases anyway.)

Then what?
----------

Supposing this goal is accepted, how do we actually get to a point where a lot of people can do this sort of thing for a lot of languages and writing systems? We build an interface that makes it possible to build orthographic inventories, and _another_ interface to map that orthographic inventory onto the IPA inventory. That's the second goal.

so

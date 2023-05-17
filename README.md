# Colors-of-DNA
### Introduction
What if you generated a colored image based on DNA?

Sounds like a weird question, but if you think about it it becomes plausible. DNA has 4 possible options per character, or nucleotide: A, C, T, or G. This could easily be converted into a binary key, using 2 bits (one of 00, 01, 10, 11) as a value for an assigned nucleotide key.

I came up with this idea just as a fun idea to mess around with, giving me practice with CLI python scripts, file I/O, and dealing with arbitrarily large datasets (genomes are often millions if not billions of base pairs long). As of writing this sentence, I haven't actually parsed any DNA strings yet so I'm quite curious as to what the outputs will look like.

However, another problem presents itself: what if the gene or genome converted into an image isn't a plain rectangular prism? For example,
if 256 pixels are coded for, a simple 16x16 image could be constructed. What about 250 pixels? The 16th row wouldn't be filled, and we'd have the choice of either padding the remaining empty 6 pixels (in this case) or cutting off the 16th row. Padding would code for extra nucleotides and removing the whole row would permanently delete some nucleotides.

Solution: each nucleotide is coded for by 3 bits rather than 2. All --1 bit sequences are to code for nucleotides, while --0 bit sequences are empty filler pixels. 

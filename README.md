# trivium
Python implementation of the trivium stream cipher

<img src="trivium_image.png" alt="example" width="400" height="400" />

Python class for the implementation of the Trivium synchronous stream
cipher. The Trivium cipher is initialized by writing an 80-bit key and
an 80-bit initialization vector (IV) to the 288-bit internal state and
updating 4 x 288 = 1152 rounds. Each subsequent update generates a
single output bit. In this implementation, the key and IV values are
input as integer lists of 1s and 0s with each instantiation.

The trivium.iterate() method carries out a single update of the three
interlinked shift registers that together compose the trivium cipher, and
appends the resulting output bit to the trivium.output attribute.

The cumulative post-initialization output bits may be retrieved by calling
the trivium.get() method.

The specifications for the Trivium cipher are available at:
https://www.ecrypt.eu.org/stream/ciphers/trivium/trivium.pdf

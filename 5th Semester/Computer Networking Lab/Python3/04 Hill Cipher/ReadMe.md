# Hill Cipher

In classical cryptography, the Hill cipher is a **polygraphic substitution cipher** based on linear algebra. Invented by Lester S. Hill in 1929, it was the first polygraphic cipher in which it was practical (though barely) to operate on more than three symbols at once. The following discussion assumes an elementary knowledge of matrices.

## Steps With Example

Each letter is represented by a number modulo 26. Often the simple scheme A = 0, B = 1, ..., Z = 25 is used, but this is not an essential feature of the cipher. To encrypt a message, each block of n letters (considered as an n-component vector) is multiplied by an invertible n × n matrix, against modulus 26. To decrypt the message, each block is multiplied by the inverse of the matrix used for encryption.

The matrix used for encryption is the cipher key, and it should be chosen randomly from the set of invertible n × n matrices (modulo 26). The cipher can, of course, be adapted to an alphabet with any number of letters; all arithmetic just needs to be done modulo the number of letters instead of modulo 26.

Consider the message 'ACT', and the key below (or GYBNQKURP in letters):

`(6	24	1	13	16	10	20	17	15)`

Consider the message 'ACT', and the key below (or GYBNQKURP in letters):

![Image Unavailable](https://github.com/MohMaya/CollegeCodes/raw/master/5th%20Semester/Computer%20Networking%20Lab/Python3/03%20Play%20Fair%20Cipher/assets/Playfair_Cipher_01_HI_to_BM.png "Step 1")

Since 'A' is 0, 'C' is 2 and 'T' is 19, the message is the vector:

<image2>

Thus the enciphered vector is given by:

<image3>

which corresponds to a ciphertext of `POH`.
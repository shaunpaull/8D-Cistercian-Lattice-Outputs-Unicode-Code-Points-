# 8D-Cistercian-Lattice-Outputs-Unicode-Code-Points-
This code creates a lattice with the specified dimensions, generates a random Unicode encryption key, and encrypts a message using the lattice and the encryption key. The encrypted message is then printed to the console.

LatticeSymbol struct: This struct represents a symbol in the lattice. It contains the following information:

symbol: An unsigned integer that represents the symbol itself.
colors: A vector of strings representing the colors associated with the symbol.
complexity: A bitset of size 512 representing the complexity of the symbol.
createLattice function: This function generates an 8D lattice with the specified dimensions (width, height, depth, time, energy, entropy, spirit, consciousness). It randomly assigns symbols, colors, and complexities to each lattice position.

encryptMessage function: This function takes a message to be encrypted, the lattice, an encryptionKey, and the number of encryption numRounds. It encrypts the message using the lattice and encryption key. Here's how it works:

It initializes an empty vector encryptedData to store the encrypted characters.
It converts the encryption key string to a vector of unsigned characters.
It sets up a random number generator and a delay distribution for simulating delays during encryption.
It iterates over each character c in the input message.
It calculates the indices (index1 to index8) in the lattice based on the character c.
It retrieves the corresponding LatticeSymbol from the lattice using the calculated indices.
It searches for the symbol with the highest complexity in the entire lattice and records its symbol value.
It performs an XOR operation between the character c, the encryption key byte at the current round, and the modulus of the highest complexity symbol, and stores the result in encryptedChar.
It appends encryptedChar to the encryptedData vector.
It adds a random delay between 100 and 1000 milliseconds to simulate a delay in the encryption process.
After all characters are processed, it converts the encryptedData vector to a string and returns it.
main function: In the main function, you can specify the dimensions of the lattice (width, height, depth, time, energy, entropy, spirit, consciousness). It calls the createLattice function to generate the lattice. It defines a message to be encrypted, generates a random encryptionKey using the generateRandomUnicodeString function, and specifies the number of encryption numRounds. It then calls the encryptMessage function to encrypt the message using the lattice and encryption key, and finally prints the encrypted message to the console.


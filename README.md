# Pressor 
## Plain Text Compressor

Mark Romphf 2024 
Implementation of [Huffman Coding](https://www.programiz.com/dsa/huffman-coding)

## Algorithm
1. Create a [priority queue](https://www.programiz.com/dsa/priority-queue) Q consisting of nodes, where each node contains:
   - A unique character
   - Its frequency
   - Pointers to left and right children (initially NULL)

2. While Q contains more than one node:
   a. Create a new node `newNode`.
   b. Extract the two nodes with the minimum frequency from Q.
   c. Set `newNode.leftChild` to the first extracted node.
   d. Set `newNode.rightChild` to the second extracted node.
   e. Set the frequency of `newNode` as the sum of the two extracted nodes' frequencies.
   f. Insert `newNode` back into Q.

3. The remaining node in Q is the root of the Huffman Tree.

4. Return the root node.


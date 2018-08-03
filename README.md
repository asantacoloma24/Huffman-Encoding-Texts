# Huffman-Encoding-Texts

# Project description:


## Goal: Implement Huffmans algorithm.

## Write a program to:
- read a file
- calculate the frequency of each character in the file
- place the characters and frequencies into a table indexed by the character
- run the character frequency through Huffmans Algorithm and create a Huffman Tree
    https://opendsa-server.cs.vt.edu/ODSA/Books/Everything/html/Huffman.html
    This site gives code for BuildTree (algorithm) HuffTree (object) and HuffLeaf that would work for this.
    You are welcome to use this code and reference it.
- traverse the Huffman Tree and print out the characters and frequencies
- read a file and encode the characters in the file using a Huffman Tree
- decode a string of 1s and 0s using a Huffman Tree

## Write a commentary on your program.
* The commentary should be a separate text, pdf, or word processing file.
* Discuss the data structures you used.  Why were they appropriate?
* Discuss the computational complexity of the operations in the Huffman Algorithm, encoding and decoding, and traversing.
* Say something about what you learned.

The assignment will be tested with the following interface.  You MUST implement this interface. The testing in its entirety will consist of running these methods and checking for correctness.

public interface HuffmanCoding

{

    //take a file as input and create a table with characters and frequencies
    //print the characters and frequencies
    public String getFrequencies(File inputFile);

    //take a file as input and create a Huffman Tree
    public HuffTree buildTree(File inputFile);
    
    //take a file and a HuffTree and encode the file.  
    //output a string of 1's and 0's representing the file
    public String encodeFile(File inputFile, HuffTree huffTree);

    //take a String and HuffTree and output the decoded words
    public String decodeFile(String code, HuffTree huffTree);

    //print the characters and their codes
    public String traverseHuffmanTree(HuffTree huffTree);
}

 

## Format for printing
For character and frequency print out there should be
character space integer newline
String charFreqTable = new String();
char myChar;
int myFrequency;
//one line of the table would be as follows:
charFreqTable = char+" "+myFrequency+"\n";
For character and code print out there should be
character space String newline
String charCodeTable = new String();
char myChar;
String myCodeString;  //string of 1s and 0s.
//one line of the table would be as follows
charCodeTable = char+" "+myCodeString+"\n";

The strings returned from traverseHuffmanTree and getFrequencies should be in ASCII order of the characters shown.

i.e. the call to getFrequencies for the file with string "!aAba" should be:

"! 1\nA 1\na 2\nb 1"

Note that '\n' is a new line character.

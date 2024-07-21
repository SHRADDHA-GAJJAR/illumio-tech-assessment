# Match Predefined Words Java Application

## Description
This Java application reads a file and finds matches against a predefined set of words. The match is case-insensitive and matches whole words only.

## Requirements
- Input file is a plain text (ASCII) file, each record separated by a newline.
- Predefined words are listed in a text file, each word separated by a newline.
- Matches should be case-insensitive.
- Match should be word-to-word, not substring matches.

## Assumptions
- The input file size can be up to 20 MB.
- The predefined words file does not contain duplicates.
- Maximum length of the word can be up to 256 characters.
- The predefined words are in English.

## How to run application
- Download zip file
- Dependency java should be installed
- Below path contains files input.text for sentences and predefinedWords.text contains predefined Word. 
	- illumio-tech-assessment/src/main/resources contains 
- Go to illumio-tech-assessment folder
- Utilize terminal to compile and run the program using the following commands
```bash or terminal
javac -d out -cp . src/main/java/matchpredefinedwords/*.java
java -cp out matchpredefinedwords.DetectWords

## I have tested below scenarios. 
- Positive
	- valid input.txt and predefinedWords.text
		- expected o/p contains Predefined word with Match count
	- Input.txt that contains case sensitive data,
		- Match count capture all occurrence of preferedWord ignoring case sensitivity
	- SubString should not be part of count. 
	
	

- Negatvie
 	- Invalid input file path 
 		--> o/p Error occurred while reading predefinedWords.text file
 	- Invalid predefinedWords file path 
 		--> o/p Error occurred while processing input.text file
 	- Empty predefinedWords 
 		--> o/p Print info message Received empty predefinedWords.text file
 	- If predefinedWords.txt are not part of input.text 
 		--> o/p Matched count as zero for all predefined word listed into predefinedWords.txt
 		
 		
 ## Further Enhancements
 
- Implement multithreading to process large input.text in parallel, improving performance. 
	- Create a class that will process a portion of the input.text.
	- Divide the input file into chunks and assign each chunk to a worker thread.
	- Combine the results from all threads at the end.
- Use streaming to handle large files more efficiently, avoiding loading the entire file into memory.
- Utilize a trie data structure for faster word matching and lookup.
 
 	
 		
 		

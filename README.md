# EntropyCalculator

EntropyCalculator is a Python tool to calculate the entropy of files, with special support for PE (Portable Executable) files. Entropy is a measure of randomness or unpredictability, which can be useful in various contexts such as cryptography and malware analysis.

## Usage

### General Usage

To calculate the entropy of an entire file:

```cmd
python3 entropycalc.py <filename>
```

### PE File Specific Usage

To calculate the entropy of individual sections within a PE file:

```cmd
python3 entropycalc.py -pe <pe_filename>
```

### Example
Whole File Entropy Calculation
```sh
python3 entropycalc.py example.exe
```
output:
```sh
Entropy Of example.exe As A Whole File Is : 4.32145
```
PE File Section Entropy Calculation
```cmd
python3 entropycalc.py -pe example.exe
```
output:
```cmd
[i] Parsing example.exe's PE Section Headers ...
    >>> "section_name" Scored Entropy Of Value: 4.32145
```
## Installation
### Requirements
Python 3.x
pefile library
Installation of Dependencies
Install the pefile library using pip:

```sh
pip3 install pefile
```

## Functions
calc_entropy(buffer)
Calculates the entropy of a given buffer.

Parameters:

buffer (str or bytes): The input buffer for which to calculate the entropy.
Returns:

float: The calculated entropy value.
calc_file_entropy(filename)
Calculates the entropy of an entire file.

Parameters:

filename (str): The path to the file.
Prints:

The entropy of the file.

### Error Handling
The script provides clear error messages for the following scenarios:

File not found
Invalid PE file

## Author
Raulisr00t

## License
This project is licensed under the MIT License.

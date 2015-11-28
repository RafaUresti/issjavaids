# Constructor Detail #


public BSReader()

> Default Constructor - this actually does nothing at the moment, but used to contain functionality for setuping up removal of "useless columns"

# Method Detail #


**public java.util.ArrayList<java.util.ArrayList<java.lang.Double>> getRange(java.lang.String filename)**

Given a filename to a comma delimited signature file, this function will parse the files and signatures into columns, and store this in a datatype. Once done parsing, each row is sorted, and the first and third quartiles are calculated and returned

> Parameters:
> > filename - The file name of the signature file

> Returns:
> > an arraylist of 41 elements, each element being an arraylist containing two elements: q1 and q3



**public static void main(java.lang.String[.md](.md) args)**


> This function is used for unit testing only.

> Parameters:
> > args -


# Example Output #
From reading in GuessPassword-TRAINING

```
Column 0 = 0.0/0.0
Column 1 = 0.0/0.0
Column 2 = 0.05/0.05
Column 3 = 0.06/0.06
Column 4 = 0.00125/0.00126
Column 5 = 0.00179/0.00179
Column 6 = 0.0/0.0
Column 7 = 0.0/0.0
Column 8 = 0.0/0.0
Column 9 = 0.1/0.1
Column 10 = 0.1/0.1
Column 11 = 0.0/0.0
Column 12 = 0.0/0.0
Column 13 = 0.0/0.0
Column 14 = 0.0/0.0
Column 15 = 0.0/0.0
Column 16 = 0.0/0.0
Column 17 = 0.0/0.0
Column 18 = 0.0/0.0
Column 19 = 0.0/0.0
Column 20 = 0.0/0.0
Column 21 = 0.0/0.0
Column 22 = 0.0010/0.0020
Column 23 = 0.0010/0.0020
Column 24 = 0.0/0.0
Column 25 = 0.0/0.0
Column 26 = 0.1/0.1
Column 27 = 0.1/0.1
Column 28 = 0.1/0.1
Column 29 = 0.0/0.0
Column 30 = 0.0/0.0
Column 31 = 0.018/0.045
Column 32 = 0.018/0.045
Column 33 = 0.1/0.1
Column 34 = 0.0/0.0
Column 35 = 0.0020/0.012
Column 36 = 0.0/0.0
Column 37 = 0.0040/0.0070
Column 38 = 0.0040/0.0070
Column 39 = 0.093/0.095
Column 40 = 0.093/0.095

```
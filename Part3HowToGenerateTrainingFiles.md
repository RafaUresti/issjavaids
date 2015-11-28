# Introduction #

For each part of this submission, we have to load different training and testing files which are specific collections of attack signatures.


# Details #

Lets use part 3 of this submission as an example:

```
Create a training set, which contains records of one attack type ( you should 
have a reasonable number, at least 20)AND records of ALL other types 
(normal and other attack types)
```

Create an empty text file, and pick 20 signatures of the attack you want.  (Straight from the unadulterated myCourses zip file).  Copy these signatures into said empty text file.

```
0, 0, 0.05, 0.07, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0.002, 0.001, 0.05, 0.1, 0, 0, 0.05, 0.1, 0, 0.001, 0.002, 0.1, 0, 0.1, 0.1, 0.1, 0.05, 0, 0
0, 0, 0.05, 0.07, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0.003, 0.002, 0.067, 0.1, 0, 0, 0.067, 0.067, 0, 0.002, 0.003, 0.1, 0, 0.05, 0.067, 0.1, 0.067, 0, 0
0, 0, 0.05, 0.07, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0.004, 0.003, 0.075, 0.1, 0, 0, 0.075, 0.05, 0, 0.003, 0.004, 0.1, 0, 0.033, 0.05, 0.1, 0.075, 0, 0
0, 0, 0.05, 0.07, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0.005, 0.004, 0.08, 0.1, 0, 0, 0.08, 0.04, 0, 0.004, 0.005, 0.1, 0, 0.025, 0.04, 0.1, 0.08, 0, 0
0, 0, 0.05, 0.07, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0.006, 0.005, 0.083, 0.1, 0, 0, 0.083, 0.033, 0, 0.005, 0.006, 0.1, 0, 0.02, 0.033, 0.1, 0.083, 0, 0
0, 0, 0.05, 0.07, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0.007, 0.006, 0.086, 0.1, 0, 0, 0.086, 0.029, 0, 0.006, 0.007, 0.1, 0, 0.017, 0.029, 0.1, 0.086, 0, 0
0, 0, 0.05, 0.07, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0.008, 0.007, 0.088, 0.1, 0, 0, 0.088, 0.025, 0, 0.007, 0.008, 0.1, 0, 0.014, 0.025, 0.1, 0.088, 0, 0
0, 0, 0.05, 0.07, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0.009, 0.008, 0.089, 0.1, 0, 0, 0.089, 0.022, 0, 0.008, 0.009, 0.1, 0, 0.012, 0.022, 0.1, 0.089, 0, 0
```

Using NewNNParser (in ISSSingleMisuseNeuralIDS), specify this file to load as well as an outputNode value for this signature.  Lets pick 2.

Now run NewNNParser.  Previously it would create the output file for you, but that sorta stopped working randomly - so create a new text file (This will be the training/testing load file for JOONE) and copy the standard output to this file.

```
0;0;0.14;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.1;0;0;0.171;0.062;0.027;0.002;0.001;0.003;0.001;0;0.029;0.002;2
0.0001;0;0.14;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.1;0;0;0.172;0.062;0.027;0.002;0.001;0.003;0.001;0;0.03;0.003;2
0;0;0.12;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.033;0.067;0;0.173;0.001;0.001;0.003;0.002;0;0.001;0;0.03;0.1;2
0.0001;0;0.12;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.05;0.05;0;0.174;0.002;0.001;0.003;0.002;0;0.001;0;0.03;0.1;2
0;0;0.12;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.02;0.06;0;0.175;0.001;0.001;0.003;0.003;0;0.001;0;0.031;0.1;2
0.0001;0;0.12;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.033;0.05;0;0.176;0.002;0.001;0.003;0.003;0;0.001;0;0.031;0.1;2
0;0;0.12;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.014;0.057;0;0.177;0.001;0.001;0.004;0.004;0;0.001;0;0.032;0.1;2
0.0001;0;0.12;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.025;0.05;0;0.178;0.002;0.001;0.004;0.004;0;0.001;0;0.032;0.1;2
0;0;0.12;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.011;0.056;0;0.179;0.001;0.001;0.004;0.005;0;0.001;0;0.032;0.1;2
```

NewNNParser takes the signatures and drops all symbolicColumns listed here on the wiki, makes sure all values are double, semicolon delimits fields, and appends the target outputNode to each signature.

Now for the "second part" of the required training data:

Empty your original text file, and select bunches of each signature type and paste them into the empty file.  Change NewNNParser to have an outputNode value of something other then the first value you selected, for example 1.

Copy the output of NewNNParser to the end of your JOONE load file.

```
0.0001;0;0.12;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.007;0.052;0;0.197;0.002;0.001;0.009;0.014;0;0.001;0;0.039;0.1;2
0;0;0.12;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.004;0.054;0;0.198;0.001;0.001;0.009;0.014;0;0.001;0;0.039;0.1;2
0.0001;0;0.12;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.007;0.052;0;0.199;0.002;0.001;0.009;0.015;0;0.001;0;0.039;0.1;2
0;0;0.12;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.003;0.053;0;0.2;0.001;0;0.009;0.015;0;0.001;0;0.04;0.1;2
0;0;0.05;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.05;0.1;0;0;0.05;0.1;0;0.001;0.002;0.1;0;0.1;0.1;0.1;0.05;0;0;1
0;0;0.05;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.067;0.1;0;0;0.067;0.067;0;0.002;0.003;0.1;0;0.05;0.067;0.1;0.067;0;0;1
0;0;0.14;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.1;0.1;0.1;0;0;0.171;0.062;0.027;0.002;0.001;0.003;0.001;0;0.029;0.002;1
```

**You now have a JOONE load file to train your neural network with!**

# Testing Data #

In the JOONE examples, they use the same load file for both training data and testing data.

For example, the first 50 lines of your JOONE load file will be training signatures, and all the lines after that will be testing signatures

```
int trainingRows = 20;
 // Extract the training data
double[][] inputTrain = JooneTools.getDataFromStream(fileIn, 1, trainingRows, 1, 34);
double[][] desiredTrain = JooneTools.getDataFromStream(fileIn, 1, trainingRows, 35, 35);
```


If you look at Misuse1.java, you will see that trainingRows is defined as an integer:  the last line your training signatures appear on.

**inputTrain** is an array of data that matches up with your input nodes on the first layer of the NN.

**desiredTrain** is the expected targets of said signatures

```
// Extract the testing data
double[][] inputTest = JooneTools.getDataFromStream(fileIn, trainingRows+1, 127, 1, 34);
double[][] desiredTest = JooneTools.getDataFromStream(fileIn, trainingRows+1, 127, 35, 35);
```

We define the testing data above, which starts at line trainingRows+1, and ends at line 127.

# Running with it man! #

After you have all your data setup, then you can jump into the pool and run your neural network.

You should get output somewhat like this:

```
Training complete.
Comparison of the last 6 rows:

Output: 0.7440024188854941 	Target: 0.5 
Output: 0.7443778729866979 	Target: 0.5 
Output: 0.9984010803183047 	Target: 0.5 
Output: 0.996610373243441 	Target: 0.5 
Output: 0.47900296761624117 	Target: 0.0 
Output: 0.4800293240062769 	Target: 0.0 
```



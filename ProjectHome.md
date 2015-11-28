# Intelligent Secure Systems IDS in Java #
Authors: Jason Laver, Nicholas Pike, Jeffery Prokop

## What is it? ##
An IDS (Intrusion Detection System) is a System designed to detect security intrusions on a given system. An intrusion detection system detects many types of malicious network traffic and computer usage that can't be detected by a conventional firewall. This includes network attacks against vulnerable services, data driven attacks on applications, host based attacks such as privilege escalation, unauthorized logins and access to sensitive files, and malware (viruses, trojan horses, and worms).

IDS' can come in two distinct flavors, **Anomaly** and **Misuse** Based IDS.

### Anomaly ###
Anomaly based detection relies upon an easily identifiable pattern of normal use. Anything that does not fall within the boundaries of this normal use is flagged as a possible intrusion. The advantage of this is that as new attacks are generated, the IDS does not necessarily need to be modified in order to counter this. Any use that is out of the ordinary is immediately flagged. Conversely, if a system does not have a regular pattern of normal use, then many false positives (good use flagged as bad) can occur.

### Misuse ###
Misuse based detection relies upon identifiable patterns and signatures of 'bad' use. Here, signatures and patterns of known bad use is used to check system use against. If use matches something known by the IDS, it is bad. Otherwise, all traffic not recognized is considered good. In a system where normal traffic cannot be easily characterized by a pattern, Misuse IDS becomes more effective since less false positives are found. However, false negatives (bad use flagged as good) can occur as new attacks not known to the system
have no problem gaining access.

## How does it work? ##
Quite simply, both IDS systems function the same way. Both rely on proper pattern recognition in order to analyze and correctly flag traffic. In order to do this, we used statistical analysis in order to create a general model for our IDS to check against.

### Step 1: Get the Data ###
First, we have to get the data that we build our data set out of. In the case of Anomaly Based IDS, we have to get a large set so examples of normal usage. For Misuse Based IDS, we have to get examples of known bad traffic and misuse. For our project, these were provided to us in the form of 41 comma delineated factors for each packet. These 41 factors are defined in the assignment document.

### Step 2: Create a Signature ###
Now that we have a large collection of data, it's time for some descriptive statistics. We will then find the Q1(first quartile) and Q3(third quartile) values for each of the factors that we are checking for. This is a way to normalize our data and remove any outliers from our data population.

### Step 3: Compare Traffic to Signature ###
Finally, all that's left is to compare an instance of traffic to our signature. This is done by simply seeing if a factor in the traffic falls within the quartile values in the factor of our signature. If this is true, our traffic has one more thing in common with our signature.

Key :: Factor=y and Traffic=X and Signature=S

Common Count = 0

FOR ALL Factors

> IF S(Q1)<sub>y</sub> < X<sub>y</sub> < S(Q2)<sub>y</sub> THEN Common Count+=1


So, how do we measure then how many commonalities dictate a flagged match to our signature? Well, we created an integer variable called a Security Level(SECURITY\_LEVEL) for just this purpose. The security level defines a number that which if the commonality count is greater than or equal to the Security Level, then we flag the traffic as matching the signature. In order to set the Security Level, we used a set of test traffic where misuse and normal usage counts were known (2200 packets, 2000 normal, 200 misuse) and ran our IDS against it until the Security Level gave us comparable results to what we knew to be good and bad in our test data.

## Developement Process ##
The workload for the development of this software is as follows:

**Nicholas Pike** : Gathering statistics - Reading in of signatures for processing
> Identifying thresholds by generating quartiles from pertinent data colums
> Parsing of data (BSReader.java) - Read in a prepare data files in a useable format

**Jason Laver** : Parsing of data (ISSBDataParser.java) - Read in a prepare data files in a useable format
> AnomalyIDS.java - Reading in, analyzing, and outputing of attack results based on thresholds

**Jeff Prokop** : MisuseIDS.java - Reading in, analyzing, and outputting of attack results based on known breaches

The team met on several occassions to coordinate work efforts and overall design.  The majority of time was spent on the implementation of the Anomaly and Misuse classes from conception to execution.

Estimated man hours = 18 - 20 hours
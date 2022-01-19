# log4jbreach
Description of the log4j Java Breach

Known as "The Most Serious Security Breach Right Now", the log4j breach is a chunk of code that recognizes, remembers and logs all recent activities that developers use when making new software. 
The issue arose when cybersecurity analysts noticed, that if you tell log4j to log a line of malicious code it automatically allows hackers to connect and control an active log4.

"Why Is Log4J so important?"
Coders have been using log4 since the mid-90's, since log4 is apart of Java's language it has been implemented in companies such as Google, Microsoft and Amazon. Even big software sellers like IBM and Oracle even use log4. 

"What Does This Mean"
Now this does not mean that everything will be hacked, but it does give hackers a sliver of leeway if they watend to attempt. Since the vuneralbility went public, coders have been working non-stop reviewing reams of code to see if they made any personal mistakes. 


Coders Method of Fixing Log4j

Option 1: Removing the JndiLookup class
This vulnerability is caused by the way Log4j uses a Java feature called JNDI (Java Naming and Directory Interface) that was designed to allow the loading of additional Java objects during runtime execution. One way to fix the vulnerability is to disable the use of JNDI message lookups, which is what Log4j 2.16.0 does. However, this can also be achieved by essentially ripping out the entire JndiLookup class, which implements this functionality, from an affected Log4j package.

Code Below:
zip -q -d log4j-core-*.jar org/apache/logging/log4j/core/lookup/JndiLookup.class


Sources Used: https://www.csoonline.com/article/3645348/how-to-properly-mitigate-the-log4j-vulnerabilities.html
https://www.washingtonpost.com/technology/2021/12/20/log4j-hack-vulnerability-java/

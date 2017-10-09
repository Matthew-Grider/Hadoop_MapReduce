#HW 2 for CS 442
U, 667867849, mgride3@uic.edu, Matthew, Grider

video: https://www.youtube.com/watch?v=A0EwR3ZvU9w&t

I used the same open source project as last hw and the source I used was pulled from my last repo here:

https://bitbucket.org/MattGrider/matthew_grider_hw1

##Collect Junit data
My project was quite large and the build is very integrated with gradle this made it hard to automate the individual creation of coverage files per test so instead of automating I produced the files instead by running jacoco.
The one thing that I did a little diffrent was because the project has quite a large amount of test (6000+) I collected data on the collection of test in each sub file
(i.e. one coverage for all tests in src/test/java/io.reactivex/internal and one coverage for each test from src/test/io.reactivex/observers etc.)

![Alt text](https://www.dropbox.com/s/avm1t5oj632bxi0/Capture.PNG)

I saved all of the jacoco html reports to a folder which I provided a replica to here:

https://www.dropbox.com/s/iha1z15ea63n6in/Coverage%20Test2.zip?dl=0

I then used the Process_Data class in my project to implment an html scraper using Jsoup library to produce a single txt file containing all the relivant data, which meant each line contained TestRan: Class-LineNum and a copy of the produced file is here:

https://www.dropbox.com/s/oiloouv73n6eprv/parsedinput.txt?dl=0

##Wrote Mapper and Ran Locally and on EMR
The rest of these steps are better shown on my youtube video:

https://www.youtube.com/watch?v=A0EwR3ZvU9w&t

To put it simply I wrote my implementation of Map Reduce in which Map would take my given input and make <Key, Value> pairs where the key was the line nubmer and the value was the test, then I would pass that to the reducer who for each key (line number) it would create a list of tests that covered it.
A copy of what the output looks like is here:

https://www.dropbox.com/s/7oyan5sdz9w67jr/output.txt?dl=0



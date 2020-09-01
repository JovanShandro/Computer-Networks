# Jovan Shandro Computer Networks Homework 4

## Homework walkthrough

For this homework I have used the latest version of bird that could be found in github, namely v2.0.2. To get this version you can follow the installation steps shown in the README [here](https://github.com/BIRD/bird/tree/v2.0.2).

For some reasons the bird6 command was not working, probably the command is not valid for this bird version so I also had to make some small changes to the mininet python script.

After running the python script:
--------
**a)** To test the network I ran ping from each node to the other. In the ping_statistics.txt file you can find the output of some of them. For some reasons ping would fail only the first time I ran it, had about 11% package loss the second time and started working perfectly for each node from the third time. Not sure what could have caused that but please make sure to check ping more than once as I think the issue is not with the network.
**b)** In the tracepath.txt file you will see the results of running tracepath from a1 to a2 once before and then after breaking down f1-eth1 using *f1 ifconfig f1-eth1 down*. You can see an alternative route was found. 
**c)** To test BGP you can see the results of running ping from a1 to b1 and b2 in pingstatistics.txt
**d)** **e)** For both these points I added filters in the common-bird.conf file. I also made a small change to what the profesor had initially given due to the bird version used. To verify these, you can check the results of running tracepath from a1 to b1 and vice-versa in the tracepath.txt file.
# Picture-Boxing

The idea for this was to create a script that would identify and box areas of large color change in a picture. Sometimes this turns out looking good, sometimes not so much.

It crops any provided photo to be a power of two to make the algorithm simple. 
It then selects a specified power of 2 and boxes the picture based on that. 

For example, if you provided a 100x1000 picture and a threshold of 64, it would create a 1x15 picture of boxes size 64 and crop the rest
It would then look through each box for a color change greater than whatever threshold provided, based on either distance from the average, maximum difference between max and min pixels. 
If the box fails this check it breaks it into 4 smaller boxes and repeats. 
# CV_final_task
Your task is to find the shaded segmentation mask.
Check out the guidelines_of_first_20_images folder. This folder is to illustrate and guide you for better understanding on the problem. 

You have to write an algorithm that will solve the following problem. Here are the instructions for your algorithm.

Inputs for the algorithm are in the dataset folder:
1. Image raw (the image folder)
2. Human parsing of the image 
3. Pose estimation of the person (both json and image) [*1]

Output:
1. The person's image with gray shaded region. Look at the sample_output.jpg for details.

Note: you don't have to use all the inputs given to you. You may use only those inputs that you find important for your algorithm to work better.



[*1]
body25 + hands labelling, check out the openpose labels for more details if you want.

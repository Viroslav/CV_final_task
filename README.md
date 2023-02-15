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

All data stored here:
https://drive.google.com/drive/folders/1pASoDgBb6ePn0gqtrxH-uRdnkUl2hz1a?usp=sharing

Solution:
I devide this task into several steps:
1) Write a function for json_points to make them more convenient to use.
2) write shaded_segmentation_mask_1 to use convexpoly and join together points of legs to make a frame
3) another function shaded_segmentation_mask_2 which iterates over segmented areas and chek if points are inside, then include them into mask (to avoid taking hand into the picture)
4) then another function to sum our frame and shaded_segmentation_mask_2
5) combine it into whole big function total
6) fill the gap if it's so

All final code in Final_task.ipynb file or in more convenient way here : https://colab.research.google.com/drive/1EaL6DaeLMWcNjEMMEodZNH93oIJPhGKb?usp=sharing

Here are some several random examples:




![https://github.com/Viroslav/CV_final_task/blob/main/1.png](https://raw.githubusercontent.com/Viroslav/CV_final_task/main/1.png)
![https://github.com/Viroslav/CV_final_task/blob/main/2.png](https://raw.githubusercontent.com/Viroslav/CV_final_task/main/2.png)
![https://github.com/Viroslav/CV_final_task/blob/main/3.png](https://raw.githubusercontent.com/Viroslav/CV_final_task/main/3.png)
![https://github.com/Viroslav/CV_final_task/blob/main/4.png](https://raw.githubusercontent.com/Viroslav/CV_final_task/main/4.png)
![https://github.com/Viroslav/CV_final_task/blob/main/5.png](https://raw.githubusercontent.com/Viroslav/CV_final_task/main/5.png)
![https://github.com/Viroslav/CV_final_task/blob/main/6.png](https://raw.githubusercontent.com/Viroslav/CV_final_task/main/6.png)


## Project: Perception Pick & Place
###Exercise 1, 2 and 3 pipeline implemented

[p1]: ./images/fig1.png
[p2]: ./images/fig2.png
[p3]: ./images/fig3.png
---

### Exercise 1, 2 and 3 pipeline implemented
#### 1. Complete Exercise 1 steps. Pipeline for filtering and RANSAC plane fitting implemented.

#### 2. Complete Exercise 2 steps: Pipeline including clustering for segmentation implemented.  

#### 2. Complete Exercise 3 Steps.  Features extracted and SVM trained.  Object recognition implemented.

All three exercises mentioned above were done. 
The snapshot of my result is shown below.

![alt text][p1]

### Pick and Place Setup

#### 1. For all three tabletop setups (`test*.world`), perform object recognition, then read in respective pick list (`pick_list_*.yaml`). Next construct the messages that would comprise a valid `PickPlace` request output them to `.yaml` format.

There were three different tabletop configurations. I got the score of acurracy 100% for test1, 100% for test2, and 87.5% for test3, respectively. 

100% (3/3) objects in test1.world
100% (4/5) objects in test2.world
87.5% (7/8) objects in test3.world

The snapshot of my result in test3 is shown below.
![alt text][p2]

#### Discussion
I spent some time to regurate the parameters for object classifications. First, I increase the value to increase the number of times to capture features for each object. So I changed i number in "for loop" from 5 to 10. Second, the color channel was transferd from RGB to HSV. I figured out that HSV transformation is effective for this object detection problem. Finally, I used "rbf kernel" for the SVM. It seems to work better than the basic linear kernel.

The confusion matrix after my alternation is shown below.
![alt text][p3]




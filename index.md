# _INTRODUCTION_ #
***

The theme for our project was Vargi bots. In this theme we are picking pakages from a shelf and segregating them into
their respective bins. The task is carried out with two UR5 arms, two logical cameras, one 2D camera and conveyor belt. 

#### **UR5 Arms** ####
These are used to carry out the pick and place functions. The packages are kept in a shelf from which they are supposed to be picked upon receiving an order. The picked package is then placed on the conveyor belt and sent towards the other Arm. The most important part to focus for this arm was the precision with which it would pick the package. The chances of collisions with external objects were high. If the package is not properly attached to the Vaccum Gripper it may collide with the shelf or other packages in it. Hence the trajectory set is such that it picks the package from the shelf and places it on the conveyor belt without any collision. It also ensures that the package is in perfect alignment with the vaccum gripper before it is turned on.

The second UR5 Arm picks the packages from the conveyor belt and drops them into their respective bins. The chances of collisions are the greates in UR5 arms. We have tried our best to set a trajectory that would avoid any collision of the arm, with or without the package. While doing this we have not neglected the fact that time taken in making the drop is just as crucial. the trajectory used is collision free and the shortest one possible.

#### **Cameras** ####
The two logical cameras are located above the conveyor belt in front of each UR5 arm. These cameras give only the package name ie., package001 etc. These cameras have been used by us to co-ordinate between the two UR5 arms as well as keeping a record of number of packages picked by the second arm. 

The colour and QR code decoding(Computer Vision techniques) is done by the 2D camera located in front of the shelf, behind the first UR5 arm. This arm is responsible for recognizing the colour of the package and hence its priority. After receiving the order, this camera is used to ensure we have picked the right package.

#### **Back-end coding** ####
As per the given study materials Python APIs are used to write the codes for the task. We have created separate nodes for each UR5 arm since the their functions are opposite to each other. Python version 2.7. 

The concepts of Python programming used were Object Oriented Programming and Threading. OOP has helped us make our codes more dynamic. We have avoided the use of hard-coding throughout the task and relied on dynamic inputs through various functions. Along with that we have utilised threading as well.

Threading is a concept used to run two nodes simultaneously. It is this concept which helps us read and decode the OR code on packages while UR5 arm is picking them from the shelf. It is alsoin action when both the UR5 arms are working at the same time.

Another language used for back-end coding is Javascript. It is used for handling the IoT tasks and Google Apps Scripts. For this task we have used Google Spreadsheets to keep a record of Inventory, Orders received, Shipping of packages and completed deliveries. The spreadsheets get updated throughout the task. Another task accomplished is email notificaton of shipment status. As soon as a package is shipped or delivered the user(for this case our team ID) gets an email of its status.

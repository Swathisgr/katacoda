The next step is to create a Dockerfile. A docker file is a text file that the Docker engine understands to automatically build an image by reading the file. The Dockerfile consists of all the commands a user would call to assemble the desired image. 
Let’s go ahead and create a Dockerfile inside the newly centos folder.
For reference, we already have a Dockerfile in ~/test directory.
We can just copy the reference Dockerfile to Centos folder.<br>
`cp ~/test/Dockerfile ~/Spark/image/centos/spark/Dockerfile`{{execute}}

To view the contents of the Dockerfile, you can use vi, vim, or cat out the contents. To view the contents in the terminal console, execute the following command:<br>
`cat ~/Spark/image/centos/Dockerfile`{{execute}}

You will now see many commands populate your terminal. These are the commands you would use if you were to install your application manually on a host. The first line of the Dockerfile determines what is the “base” image you will be using to install your application on. Blue Data provides their own base image, which you can use by simply putting the following command at the top of your Dockerfile: 
FROM bluedata/centos7:latest
All the commands proceeding the base image, are the commands used to setup the application. These files / commands will be setup on top of the base image from BlueData and will eventually compile into a .Bin file for use on the EPIC platform. 

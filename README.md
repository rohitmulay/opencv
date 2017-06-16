# opencv
<b><h2>Installation of OpenCV C++ library on a Linux(Ubuntu 16.04) operating system.</h2></b> 

First, make sure that your terminal has access to the internet. (If you are using a Proxy network please visit https://github.com/rohitmulay/setproxy )

Then, Update and Upgrade using the following commands: 

`sudo apt-get update`        # Fetches the list of available updates

`sudo apt-get upgrade`       # Strictly upgrades the current packages

`sudo apt-get dist-upgrade`  # Installs updates (new ones)

Download <b>OpenCV-3.2.0.zip</b> (The Latest Version) from http://opencv.org/ and place it in one directory say “opencvdrive”. 

Then download <b>opencv.sh</b> shell script from this  <a href="https://github.com/rohitmulay/opencv">repository</a> and extract it in the same directory (opencvdrive).

Now open the terminal in that directory
 <a href="https://ibb.co/eOX27k"><img src="https://preview.ibb.co/mx39nk/Picture1.png" alt="Picture1" border="0" /></a>

Run the shell script <B>opencv.sh</B> which will automatically install all the required files and libraries of OpenCV from the internet using sudo commands. (If Permission is denied, Give the command chmod 777 opencv.sh). 
<a href="https://ibb.co/cvEM05"><img src="https://preview.ibb.co/npNVtQ/Picture2.png" alt="Picture2" border="0" /></a> 

After all the commands have ran properly you will get a message on the terminal “<b>opencv 3.2.0 ready to be used</b>” this means you are good to go forward now. 

Then in the terminal give the command
       <b>pkg-config --cflags opencv</b> 
The output should be: 
     <b> -I/usr/local/include/opencv -I/usr/local/include <b>

Then in the same terminal give the command <b>pkg-config --libs opencv</b>
The output should be: <b>-L/usr/local/lib -lopencv_shape -lopencv_stitching -lopencv_objdetect -lopencv_superres -lopencv_videostab -lopencv_calib3d -lopencv_features2d -lopencv_highgui -lopencv_videoio -lopencv_imgcodecs -lopencv_video -lopencv_photo -lopencv_ml -lopencv_imgproc -lopencv_flann -lopencv_core</b>
<a href="https://ibb.co/bR92q5"><img src="https://preview.ibb.co/hhVWiQ/Picture3.png" alt="Picture3" border="0" /></a>

If you get the above outputs you are now good to run a OpenCV program which can be in C/C++, Python or Java…etc.

To compile a OpenCV program you have to give the command: <b>"g++ \`pkg-config --cflags opencv\` filename.cpp \`pkg-config --libs opencv\` </b> and then <b> ./a.out</b> to run it. ( In this command (\`) is a backtick not single quotation or single inverted commas (') )

<a href="https://ibb.co/nPVxOQ"><img src="https://preview.ibb.co/b5UDxk/Picture4.png" alt="Picture4" border="0" /></a>

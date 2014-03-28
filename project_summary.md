# Life by time


## Authors
- Terus, Limsurut, few2012few
- Pornpawit Trikumpun ,zinzoz


## Description
We started from the brainstorm to find a topic of interesting with this work then we choose the concept about light. After we find the information of light. We have concluded that it is specifically to research about time and period.
 
Experiment
Light: I've tried taking multiple images at one time, by the alpha =1/number of picture: example; if to each image of the sea several times. That picture will try to reduce the difference of all. Make the sea that looks like no wave **
Sound:

Function
-LED: a change in the light of the Sun.

-Smoke: Instead of moving clouds.

-Water: Water can make the overlapping images, but it still value of the clarity. 

-Music: the story of the inroads of time.

-Smell: a mood to people's feelings.


We use all information to present the installation art, which relate with Life such as emotion and time.


## Link to Prototype
https://www.youtube.com/watch?v=rn7UTz9lUaU

Credit paktaifarang


## Example Code
Code : overlap of image (Alpha value of each = 1 / n)
```
#include <opencv2/opencv.hpp>
#include <opencv2/highgui/highgui.hpp>
#include <iostream>

using namespace cv;
using namespace std;
int main()
{
    double alpha ; double temp;
    double npic=100;
    Mat src[150];
    /// Read image ( same size, same type )
    src[1] = imread("/Users/sharnonsharnon/Documents/opencv-2.4.8/xcodefuse/testproject2/testproject2/p31.jpg",1);
    ...[_] = ...
    
    alpha = 1/(npic);
    temp=alpha;
    for(int i=1;i<=npic;i++)
        if( !src[i].data ) { printf("Error loading src %d \n",i); return -1; }
    
    /// Create Windows
    cvNamedWindow("Linear Blend", 1);
	   alpha = 1/(npic);
    temp = alpha;
        for(int j=1;j<=npic-1;j++)
        {
            addWeighted( src[j], alpha, src[j+1], temp , 0.0, src[j+1]);
            alpha = 1;
            
            imshow( "Linear Blend", src[j+1] );
        }
    waitKey(0);
    cvDestroyWindow("Linear Blend");
    return 0;
}
```


## Images & Videos
Experiment-Light 

Test1
![Experiment light :##test1](/project_images/test1-1.jpg "Experiment light -##test1"),

**You can see all picture in my gitgub : /project_images/Experiment/Light/test1-test6)

Test2
![Experiment light :##test2](/project_images/test2-2.jpg "Experiment light -##test2"),

Test3
![Experiment light :##test3](/project_images/test3-3.jpg "Experiment light -##test3"),

Test4
![Experiment light :##test4](/project_images/test4-4.jpg "Experiment light -##test4"),

Test5
![Experiment light :##test5](/project_images/test5-5.jpg "Experiment light -##test5"),

Test6
![Experiment light :##test6](/project_images/test6-6.jpg "Experiment light -##test6")

**You can see all picture in my gitgub : /project_images/Experiment/Light/test1-test6)



##Operation

![Overview](/project_images/operator.jpg "Overview")



##Placement-installation art

![Overview](/project_images/Placement-installation art.jpg "Overview")





-Software

1. Input user's emotional

2. Sound in folder will open depends on user's emotional

                                                                                                      
-Hardware

1.LED controller (based to sound)

2.diffuser+aroma controller

3.water fall controller( on /off)



##Software

-Light+Sound

 Getting the mood I interpret the selected folder or send the array. The folder is  will be checked again  with condition. If it runs across the music of the song, the midi data is sent out to retrieve the code to play sound and light.


![Overview](/project_images/soft.png "Overview")

Controlling GPIO from MIDI events
Music from MIDI files using the music player on the other side Timidity on the subject of light is the sequence of the C programming language MIDI.

```
#include <alsa/asoundlib.h>
#include <wiringPi.h>
#include <limits.h>
#include <unistd.h>
#include <math.h>

int main()
{

    //Start as a daemon
    if( daemon(0,0) != 0) {
      exit(1);
    }
    
    //Setup wiringPi
    if( wiringPiSetup() == -1) {
      exit(1);
    }
   
    //Setup all the pins to use OUTPUT mode
    int i=0;
    for(i=0; i< TOTAL_PINS; i++) {
      pinMode(i, OUTPUT);
    }


    clearPinsState();

    //Open a midi port, connect to thru port also
    midi_open();

    //Process events forever
    while (1) {
       midi_process(midi_read());
    }

    return -1;
}
```
**Use WiringPi to control relays connected to the light



##Hardware

-Light+Sound

-Raspberry Pi to controll LED
https://www.youtube.com/watch?v=Q6U2Bi5NK6Q#t=19

Credit Kevin Darrah




##Principles of this installation art


![Animation](/project_images/projectDEV-art.gif "Animation project")




We hope this installation will allow the user to feel relaxed mood over 
the response of this work which presented in a colorful format.

: )________________T-T_________________: (__________________________><

**Sorry i have problem.I can't delete some post is same page .Althought it don't have this post in grit,but that post don't disappear .**


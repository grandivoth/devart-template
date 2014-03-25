# Project Title
Life by time

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
https://www.youtube.com/watch?v=FehBLNHMlfo


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
## Links to External Libraries
http://www.google.com

## Images & Videos
Experiment-Light 

![Experiment light :##test1](/project_images/test1-1.jpg "Experiment light -##test1"),

![Experiment light :##test2](/project_images/test2-2.jpg "Experiment light -##test2"),

![Experiment light :##test3](/project_images/test3-3.jpg "Experiment light -##test3"),

![Experiment light :##test4](/project_images/test4-4.jpg "Experiment light -##test4"),

![Experiment light :##test5](/project_images/test5-5.jpg "Experiment light -##test5"),

![Experiment light :##test6](/project_images/test6-6.jpg "Experiment light -##test6")


##Software/Hardware
-Software

1.Input emotion

2.Open sound in folder which follow to emotion

3.Send information to hardware.

-Hardware

1.Recieve information and tranformation to potocol

2.LED controller (adrdunio)

3.Smook controller


##Overview
![Overview](/project_posts/10004018_10152295985161605_1255508204_n.jpg "Overview"),


updating...



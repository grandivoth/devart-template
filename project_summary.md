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

-Music: the story of the inroads of time./n
-Smell: a mood to people's feelings.


We use all information to present the installation art, which relate with Life such as emotion and time.

## Link to Prototype
//dropbox

## Example Code
NOTE: Wrap your code blocks or any code citation by using ``` like the example below.
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
 NOTE: You can also use this space to link to external libraries or Github repositories you used on your project.

[Example Link](http://www.google.com "Example Link")

## Images & Videos
Experiment
-Light 


updating...

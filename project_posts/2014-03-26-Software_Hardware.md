
-Software

1.Input emotion

2.Open sound in folder which follow to emotion



-Hardware


1.LED controller (base to sound)

2.diffuser+aroma controller

3.water fall comtroller( on /off)



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

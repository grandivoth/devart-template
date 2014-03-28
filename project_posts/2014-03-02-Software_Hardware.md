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

![Overview](/project_posts/10004018_10152295985161605_1255508204_n.jpg "Overview")


##Software

 Getting the mood I interpret the selected folder or send the array. The folder is  will be checked again  with condition. If it runs across the music of the song, the midi data is sent out to retrieve the code to play sound and light.
 
https://www.youtube.com/watch?v=Fb8107XZ8oI#t=59
 
 
 a Midi file is fed into Linux’s ALSA midi sequencer service, destined to be played on a particular port.  The sequencer then broadcasts accurately timed midi events to all programs subscribed to said port.  One of those programs is Timidity, which is a free midi synthesizer that will take care of playing the sound.  The other is a simple C program that I wrote to  control the GPIO pins based on midi events.  Each GPIO pin controls a solid state relay, which ultimately toggles the main electricity  going to each bank of  lights.

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

-Raspberry Pi to controll LED
https://www.youtube.com/watch?v=Q6U2Bi5NK6Q#t=19

credit Kevin Darrah

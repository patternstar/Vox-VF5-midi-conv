# Vox-VF5-midi-conv
A reaper JS script to convert the 0-127 MIDI control messages to separate MIDI note on/off messages

I discovered that my Vox VF5 foot pedal can be plugged into the foot controller input of my Yamaha digital piano.  I wrote this script so I could use the pedal as a midi controller input for looping software.

Pushing switches on the VF5 creates discrete voltage levels on the output. The piano (and possible other compatible midi hardware) will convert these levels to midi values in the range 0 - 127.  Usualy these will be control values for "foot controller" (04).  To be useful the script separates these into midi note on and note off messages.  It aslo has very basic smarts to ensure only one note on / note off pair can be created at a time and avoids spurious noise.

The intended downstream input for these MIDI messages is the sooperlooper looping software however this script can be used or adapted for use for a variety of applications.

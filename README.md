# PitchPerfect
Udacity IOS Nanodegree Project 1
Test the App

To run this app, please do the following:

Download it to your computer using one of the download links above, from the GitHub project page or from my portfolio page on the right-hand side.
Once downloaded, open the project folder and then open the Pitch Perfect.xcodeproj file.
Make sure that you are testing the application on a device that it will run efficiently on (see build information on the right.)
I recommend running it on an iPhone 6 or newer, but it will run fine on anything newer than an iPhone 4S.
If you are using the iPhone Simulator, please run it on a newer device such as the iPhone 6 or 6S Plus. It should be compiled with XCode 7.0 or 7.1 in Swift 2.0. I will update it over time when new versions of XCode are released.


If you don't want to run it or can't for some reason, take a look at the video at the top of the page or screenshots below. You can follow along with the video, or read the instructions below.

Project Specifications

The Pitch Perfect app allows users to record a sound using the device’s microphone. It then allows users to play the recorded sound back with six different sound effects / filters. The application uses AVFoundation to record, play and apply sound effects to the recording. The sound effects are enumerated below. 1. Snail (Slow Playback) 2. Rabbit (Fast Playback) 3. Chipmunk (High Pitch) 4. Darth Vader (Low Pitch) 5. Parrot (Echo) 6. Reverb

Record Sounds View

The record sounds view is the initial view for the app, and consists of a button with a microphone image. A label indicates that you should tap the button to start recording is located beneath the image.

Tapping this microphone button starts an AVAudio recording session. The app uses code from AVFoundation to record sounds from the microphone. As the app is recording, the microphone button animates, using a custom UIKit animation function called FadeInAndOut. Adding this animation was my first attempt at utilizing Swift class extensions.

Tapping the button disables the record button, display a “recording” indicator label, and presenting a stop button. For extra credit, this app presents you with the ability to pause and restart recordings in addition to stopping them by interacting with the audio playback controls.

When the stop button is clicked, the app completes its recording and then pushes the second scene (described below under “Play Sounds View”) onto the navigation stack. The title in the navigation bar appears as “Record”.

Play Sounds View

The play sounds view has four buttons to play the recorded sound file and a button to stop the playback.

The buttons for playing the recorded sounds have images corresponding to their sound effect:

Chipmunk image → High-pitched sound
Darth Vader image → Low-pitched sound
Snail image → Slow sound
Rabbit image → Fast sound
Parrot → Echo
Overlapping Waveforms → Reverb
Additional sound effects, such as reverb and echo, were implemented and added to this view for extra credit.

The play sounds view is pushed onto the navigation stack. At the top left of the screen, the navigation bar’s left button says “Record”. Clicking this button will pop the play sounds view off the stack and return you to the record sounds view.

At this point, the play sounds view will be in its original state. The microphone button will be enabled and the stop button will be hidden.

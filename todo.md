p5.sound to do list
========

### This is a list of things that we hope to accomplish with p5.sound. If you want to work on one of these, or discuss an idea, feel free to make a github issue. Got something to add to the list? We'd love to hear it!


- Incorporate the new [Stereo Panner Node](http://webaudio.github.io/web-audio-api/#the-stereopannernode-interface), with a fallback to the existing panner for browsers that don't yet support StereoPanner.


- p5.Amplitude normalize method should be dynamic. It can accept a parameter that determins how fast it decays.


- Figure out a way to keep track of connections between objects. From there, .disconnect() can accept a specific object rather than disconnecting all output.


- Make sure all methods that should be modular can accept a Number, AudioParam, p5.Env, p5.Oscillator or p5.Signal as input.


- Log a message to the console if a user calls FFT methods like getEnergy without first calling .analyze() in either the draw loop, or in the method in which they call getEnergy. Maybe log the time that .analyze was last called, and compare it to the current time, and if it is a big gap, then log the message?


- SoundFile.playMode('untilDone') would play a sound if not already playing, but if it is already playing, it would not play again until it is done. Feel free to re-open this [Github Issue](https://github.com/therewasaguy/p5.sound/issues/5) if you want to work on this.


- Improve p5.Pulse (PWM)


- What additional features/analysis would be useful for visualization / analysis? Look into handling these with an offline audio context, and/or scripts that could analyze a file and then save the result to JSON.
  * Peak Detect https://github.com/therewasaguy/p5.sound/issues/12
  * Beat Detect -- [here's an example](http://tech.beatport.com/2014/web-audio/beat-detection-using-web-audio/) handled by an offline audio context
  * Pitch detect -- [here's an example](https://webaudiodemos.appspot.com/pitchdetect/index.html).


- Enhance the examples from [p5 music viz workshop repo](https://github.com/therewasaguy/p5-music-viz) and make these more accessible, perhaps as a section of p5js.org. Some useful examples to add:
  * Creating and working w/ lyric files (LRC) or other timestamped data
  * Synthesizing musical patterns (i.e. with p5.Part) and mapping these to visuals
  * Using the p5.dom library to add a drag-and-drop area for mp3s (examples currently use custom dragfile.js)
  * Loading music to p5.SoundFile from external API’s


- Build a prototype for a p5.Synth.
  * Pubilsh a spec for how synths should behave that enables people to add/share their own instruments.
  * Figure out how to handle voice allocation.
  * Including some nice sounding [custom oscillator periodicwaves](http://webaudio.github.io/web-audio-api/#the-periodicwave-interface)


- Build out current effects and develop new ones.
  * Publish a spec so that people can easily share/add custom effects
  * How best to apply an effect like p5.Reverb to all sound in the sketch? Perhaps p5.soundOut gets a wet/dry effects bus.


- Mixer and Wet/Dry


- Prepare to implement the [AudioWorker](http://webaudio.github.io/web-audio-api/#the-audioworker), because ScriptProcessor will soon be depricated. We'll likely need a fallback during this transition.

 
- Write tests and benchmark performance.


- Find and optimize areas of slow performance.


- Improve documentation and examples when you see anything that is unclear.

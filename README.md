# Anal~
An application that analyzes an audio input and that outputs OSC packets. Made with Cyling '74's Max.

## Build

Requires segment~ and analyzer~ by Tristan Jehan (http://web.media.mit.edu/~tristan/maxmsp.html). A copy of the externals are included in the repository.The main patcher is "_anal~.maxpat", but the main window is "anal~.maxpat". Do not forget to include "fftw3.dll" for a windows build.

## OSC output

* ```/fft floatx25``` : the fft analysis of the audio input between 0.0 and 1.0 spread over 25 bands.
* ```/level float``` : the level of the signal between 0.0 and 1.0.
* ```/segment float``` : onset detected with its loudness variation curve between 0.0 and 1.0.
* ```/brightness float``` : brightness estimator (spectral centroid measure) between 0.0 and 1.0.
* ```/noisiness float``` : noisiness estimator (bark-based spectral flatness measure) between 0.0 and 1.0.
* ```/note float float``` : midi note detection in pitch and velocity pairs (in the range of 0 to 127).

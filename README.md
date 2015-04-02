# Anal~
An application that analyzes an audio input and that outputs OSC packets. Made with Cyling '74's Max.

## Build requirements

Requires segment~ and analyzer~ by Tristan Jehan (http://web.media.mit.edu/~tristan/maxmsp.html). A copy of the externals are included in the repository.

## Build

The main patcher is "_anal~.maxpat", but the main window is "anal~.maxpat".

## OSC output

* ```/fft 25xfloat``` : the fft analysis of the audio input in the range of -96 to 30.
* /level float : the level of the signal in the range of -120 to 30.
* /segment float : onset detected with its loudness variation curve.
* /brightness float : brightness estimator (spectral centroid measure) in the range of 0 to 22000.
* /noisiness float : noisiness estimator (bark-based spectral flatness measure) in the range of 0 to 1.
* /note float float : midi note detection in pitch and velocity pairs (in the range of 0 to 127).

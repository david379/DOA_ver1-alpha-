# DOA_ver1-alpha-
Necessary Imports: math, numpy, scipy.fft, pandas, time, scipy.io, soundfile. Please verify that all of those modules are installed.

The primery function is DOA_ang, while all of the other files are secondary functions required for it to work. The function takes no inputs, but assumes the existance of the 3 folders in the repository.
It assumes that the audio folder contains an audio file named "signal-1.wav' which is a 8-channel 32k sample rate WAV file, which is 50ms long (if it is longer the function takes only the first 50ms and ignores the rest).
The function outputs an azimuthal angle which it believes to be the DOA of the sound. 
the DOAs and mic_arrays folders contain MAT files created offline in a seperate matlab code which generate the DOA vectors and time delays assosiated with the selected search grid, and the configuration of the mic array on the platform.

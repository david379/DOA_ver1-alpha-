# DOA_ver1-alpha-
Necessary Imports: math, numpy, scipy.fft, pandas, time, scipy.io, soundfile, pyfftw. Please verify that all of those modules are installed.

The primery function is DOA_ang, while all of the other files are secondary functions required for it to work. The function takes no inputs, but assumes the existance of the 3 folders in the repository.
It assumes that the audio folder contains an audio file named "signal-1.wav' which is a 8-channel 32k sample rate WAV file, which is 50ms long (if it is longer the function takes only the first 50ms and ignores the rest).
The function outputs an azimuthal angle which it believes to be the DOA of the sound. 
the DOAs and mic_arrays folders contain MAT files created offline in a seperate matlab code which generate the DOA vectors and time delays assosiated with the selected search grid, and the configuration of the mic array on the platform.

Second version notes: a new function has been added, Process, which assumes a full audio file exists in the "audio" folder under the name "signalOG.wav". the function splits the file into equal 50ms slices and runs "DOA_ang" on each one, creating a list of tuples in the shape of (time, angle). The function also implements a primitive denoising algorithm, which deletes isolated peaks. Also, some aspects of the DOA calculation have been improved to speed up the calculation time, such a providing a cutoff frequency of 8khz and slight code optimization.

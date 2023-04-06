### Description
Usage of denoiser in input audio for ASR applications


# Denoiser with Fine Tuned Model

## Intro

The following source code showcases the use of the "Denoiser" on the input audio file to a pre trained
"Whisper" model using a REST API built on "Flask", where the file is curled nd transcript is returned.

## Denoiser

THe denoiser is a causal speech enhancement model working on the raw waveform that runs in real-time on a laptop CPU.
The proposed model is based on an encoder-decoder architecture with skip-connections. It is optimized on both time and frequency domains, using multiple loss functions. Empirical evidence shows that it is capable of removing various kinds of background noise including stationary and non-stationary noises, as well as room reverb.
Additionally, we suggest a set of data augmentation techniques applied directly on the raw waveform which further improve model performance and its generalization abilities.

Installation details and more information about the denoiser can be found below in facebook's website:
https://github.com/facebookresearch/denoiser

## Running the file

flask --app file_name run

Curling audio files:
curl -F file=@audio_filename.wav localhost:5000

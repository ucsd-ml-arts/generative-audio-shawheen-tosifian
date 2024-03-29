# Project 2 Generative Audio

Shawheen Tosifian, stosifia@ucsd.edu


## Abstract

The goal for this project is to use the pre-trained NSynth model provided by Google's Magenta, called E-Z NSynth, to interpolate sounds between two different sound clips and ideally create an output that mixes the melodic representation of one clip with the ambient 'texture' of the other. One clip would be of an ambient sound recording, such as rain outside a window or wind rushing through a forest opening, and the other would be a melodic sample from an instrument, such as a guitar lick or a piano chord progression. The inspiration behind the mixing of these two types of clips is to create an audio 'texture' similar to that of guitar effects pedals, where each effect is defined using a descriptor often alluding to a sound that we might be familiar with our 'everyday' experiences. An appropriate example might be that of the Dunlop Cry Baby Wah-Wah Pedal, being described as wah wah pedal due to its effect on making the guitar sound like it's a frustrated, dramatic toddler (essentially personifying the instrument). Another case would be a fuzz pedal, which distorts the guitar to the point where the word 'fuzzy' would be an apt descriptor of the sound.

By letting the neural network interpolate between these sounds, we allow it to explore textures that might not normally be available to conventional audio effects, with the hope that somewhere along the process it might create usable effects that mimic the ambient source audio in the same manner a fuzz or wah wah effect would make a guitar or piano sound 'fuzzy' or like a crying baby (respectively).

This was carried out by uploading the two sounds that I wanted to mix/interpolate to the E-Z Synth model run on Google Colab (link provided below to colab notebook). The model would then encode the sounds, then synthesize their encodings and interpolation between the two, which is what we're primarily after. This interpolation would be the mixing of the ambient and melodic sounds.


I went through a lot of effects, but the ones I found most interesting are included in the repository. Their descriptions can be found below

For a lot of the sound combinations, there wasn't much success in achieving a mixing as described before between the ambient sound and melodic one, let alone something that is listenable. The combinations that were closest to the intended outcome were that of the underwater sound, which only seemed to have a low-pass filtering effect on the audio. The interpolations were weak partly due to the encoding not being representative of the original audio, with a lot of them having harsh, distorted artifacts in them (like a broken violin).

A future direction could be taken using a style transfer approach on spectrograms of each audio clip in the hopes that certain 'qualities' of the ambient sound can be transferred to the melodic clip


## Data


The sound clips (ambient noises and distorted guitar lick and saxophone) fed into the model were obtained from freesound.org with the clips of guitar, piano, and 808 drum kit produced/recorded using GarageBand.

A pair of source audio files are included in each directory with their respective encodings and interpolation.

## Code

Code used for this project can be found at:
https://colab.research.google.com/drive/12F_kdZVwAxtqMztU1tREOGw-chQjaScl#scrollTo=hEAhqBo3EaEO


## Results

Description of each directory and its contents:

crybaby_lick: Ambient sound is of baby crying. Melodic sound is of undistorted electric guitar playing a Jimi Hendrix lick. Includes their encodings and interpolation, with the intention of baby crying to have a 'wah-wah' effect (it did not)

fire_lick: Ambient sound is a crackling campfire. Melodic sound is of a distorted electric blues lick. Includes their encodings and interpolation.

rain_fingerpick: Ambient sound is rain pattering outside a studio. Melodic sound is a finger-picked electric guitar progression. Includes their encodings and interpolation.

rain_lick: Ambient sound is rain pattering outside a studio. Melodic sound is a finger-picked electric guitar progression. Includes their encodings and interpolation.

underwater_808: Ambient sound is a recording taken underneath a river. Melodic sound is a beat made using an 808 drum kit. Includes their encodings and interpolation.

underwater_piano: Ambient sound is a recording taken underneath a river. Melodic sound is a a chord held down on a MIDI Grand Piano. Includes their encodings and interpolation.

underwater_song: Ambient sound is a recording taken underneath a river. Melodic sound is an 8 second sample of the salsa song Sin Poderte Hablar by Willie Colón




## Technical Notes

Processing was done on Google Colab
When running block for uploading files, may need to rerun in order to upload files

## Reference

More on NSynth can be found in the paper 'Neural Audio Synthesis of Musical Notes with WaveNet Autoencoders' by the Magenta Team

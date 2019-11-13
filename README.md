# Project 3 Generative Audio

Shawheen Tosifian, stosifia@ucsd.edu


## Abstract

The goal for this project is to use the pre-trained NSynth model provided by Google's Magenta, called E-Z Synth, to interpolate sounds between two different sound clips and ideally create an output that mixes the medlodic representation of one clip with the ambient 'texture' of the other. One clip would be of an ambient sound recording, such as rain outside a window or wind rushing through a forest opening, and the other would be a melodic sample from an instrument, such as a guitar lick or a piano chord progression. The inspiration behind the mixing of these two types of clips is to create an audio 'texture' similar to that of guitar effects pedals, where each effect is defined using a descriptor often alluding to a sound that we might be familiar with our 'everyday' experiences. An appropriate example might be that of the Dunlop Cry Baby Wah-Wah Pedal, being described as wah wah pedal due to its effect on making the guitar sound like it's a frustrated, dramatic toddler (essentially personifying the instrument). Another case would be a fuzz pedal, which distorts the guitar to the point where it word 'fuzzy' would be an apt descriptor of the sound.

By letting the neural network interpolate between these sounds, we allow it to explore textures that might not normally be available to conventional audio effects, with the hope that somewhere along the process it might create usable effect that mimics it source ambient audio in the same manner a fuzz or wah wah effect would make a guitar or piano sound fuzzy or like a crying baby (respectively).

This was carried out by uploading the two sounds that I wanted to mix/interpolate to the E-Z Synth model run on colab (link provided below to colab notebook). 


I went through a lot of effects, but the ones I found most interesting are included in the repository

A future direction could be taken using a style transfer approach (using spectrograms)


Results:


Include your abstract here. This should be one paragraph clearly describing your concept, method, and results. This should tell us what architecture/approach you used. Also describe your creative goals, and whether you were successful in achieving them. Also could describe future directions.

## Model/Data

Briefly describe the files that are included with your repository:
- trained models
- training data (or link to training data)

## Code

Your code for generating your project:
- Python: generative_code.py
- Jupyter notebooks: generative_code.ipynb

## Results

Documentation of your results in an appropriate format, both links to files and a brief description of their contents:
- `.wav` files or `.mp4`
- `.midi` files
- musical scores
- ... some other form

## Technical Notes

Any implementation details or notes we need to repeat your work. 
- Does this code require other pip packages, software, etc?
- Does it run on some other (non-datahub) platform? (CoLab, etc.)

## Reference

References to any papers, techniques, repositories you used:
- Papers
- Repositories
- Blog posts

# GuitarModes
Blending my passion for guitar with my desire to learn software development.

## Overview
I have been playing guitar for 13 years. Until this spring, I did not know any music theory beyond a few things:
* Major / Minor Triads
* Pentatonic Scale (Four-Five frets worth)
  * Flattened Fifth Note
* Major Scale from the Ionian Mode through the first octave of Phrygian.

Recently, I have been learning music theory. It's dramatically changed the way I see the guitar. A ton of things are falling into place. (Learning songs, writing music, being able to think of my riffs in terms of notes, etc...)

This project is the synthesis of my desires to learn software development and music theory. This application will provide the user with tools to practice scales and other music theory bits.

## Plans
### My plans from basic to incredibly ambitious are:
 - [x] Establish a way to generate a fretboard in plaintext that reflects a theoretical fretboard.
 - [ ] Integrate hz and octaves, differentiate based on that instead of arbitrary index values.
 - [ ] Dynamically emphasize different notes corresponding to different music theory concepts.
 - [ ] Implement ASIO integration--monitor input--come up with a very basic Rocksmith type thing for practicing.
 - [ ] Make a mobile version.

### Examples:
* What's a full tone higher than a C note?
* To which major or minor scale does C Locrian belong?
* To which scale does the following sequence of notes belong? 
 * C-D-E-F-G-A-B-C
* The highlighted notes belong to which scale?
* The highlighted notes belong to which mode?
* What are the notes of the C Dorian Mode?

## Anticipated Changes
* Ability to use either sharp or flat notes. 
  * Typically, Major keys' B, E, A, D, and G's accidentals are referred to by flats and not sharps.
  * Typically, Minor keys' B and E's accidentals are referred to by flats and not sharps.
* Depending on how I approach the algorithms to quiz you on key signatures / scale positions / modes...
  * It's going to be a problem that the current system cannot account for octaves of notes. I may simply have to use frets as a fulcrum.

## Changelog

### Version 0.5 - 2022/05/08
* First Working Version
  * I'm going to break this going forward.
  * I need to implement a method to differentiate between keys via hz and octave. Currenly everything is just relative to some indexes I came up with.
  * More information here: https://www.ece.iastate.edu/~alexs/classes/2016_Spring_575/HW/HW5/files/piano-key-freq-wikipedia.pdf 


### Version 0.4 - 2022/04/19
* Neglected changelog for three weeks
* Refactored some bits.
* Added the ability to generate modes and select them.

```
#  sample output
Key of F.
F key signature: 
['F', 'G', 'A', 'A#', 'C', 'D', 'E', 'F']
F Ionian
['F', 'G', 'A', 'A#', 'C', 'D', 'E', 'F']
G Dorian
['G', 'A', 'A#', 'C', 'D', 'E', 'F', 'G']
A Phrygian
['A', 'A#', 'C', 'D', 'E', 'F', 'G', 'A']
A# Lydian
['A#', 'C', 'D', 'E', 'F', 'G', 'A', 'A#']
C Mixolydian
['C', 'D', 'E', 'F', 'G', 'A', 'A#', 'C']
D Natural Minor (Aeolian)
['D', 'E', 'F', 'G', 'A', 'A#', 'C', 'D']
E Locrian
['E', 'F', 'G', 'A', 'A#', 'C', 'D', 'E']
```

### Version 0.3 - 2022/04/01
* Implemented intonation flag.
* I'm tired

```
# Sample output
A# minor
['A#', 'C', 'C#', 'D#', 'F', 'F#', 'G#', 'A#']
Fb minor
['E', 'F#', 'G', 'A', 'B', 'C', 'D', 'E']
```


### Version 0.2 - 2022/04/01
* renamed python files for fretboard and scales
* created a functional generator for scales of both major and minor, without a working flag for sharpness
```
# Sample output
MAJOR SCALES
         A major
         ['A', 'B', 'C#', 'D', 'E', 'F#', 'G#', 'A']
         B major
         ['B', 'C#', 'D#', 'E', 'F#', 'G#', 'A#', 'B']
         C major
         ['C', 'D', 'E', 'F', 'G', 'A', 'B', 'C']
         D major
         ['D', 'E', 'F#', 'G', 'A', 'B', 'C#', 'D']
         E major
         ['E', 'F#', 'G#', 'A', 'B', 'C#', 'D#', 'E']
         F major
         ['F', 'G', 'A', 'A#', 'C', 'D', 'E', 'F']
         G major
         ['G', 'A', 'B', 'C', 'D', 'E', 'F#', 'G']
MINOR SCALES
         A minor
         ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'A']
         B minor
         ['B', 'C#', 'D', 'E', 'F#', 'G', 'A', 'B']
         C minor
         ['C', 'D', 'D#', 'F', 'G', 'G#', 'A#', 'C']
         D minor
         ['D', 'E', 'F', 'G', 'A', 'A#', 'C', 'D']
         E minor
         ['E', 'F#', 'G', 'A', 'B', 'C', 'D', 'E']
         F minor
         ['F', 'G', 'G#', 'A#', 'C', 'C#', 'D#', 'F']
         G minor
         ['G', 'A', 'A#', 'C', 'D', 'D#', 'F', 'G']
```

### Version 0.1 - 2022/03/31
Everything you see here:
* Goals described
* Made a method to generate all the notes of a fretboard
* I'm tired.

```
# Sample output
['E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B', 'C', 'C#', 'D', 'D#', 'E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B', 'C', 'C#', 'D', 'D#', 'E']
['A', 'A#', 'B', 'C', 'C#', 'D', 'D#', 'E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B', 'C', 'C#', 'D', 'D#', 'E', 'F', 'F#', 'G', 'G#', 'A']
['D', 'D#', 'E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B', 'C', 'C#', 'D', 'D#', 'E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B', 'C', 'C#', 'D']
['G', 'G#', 'A', 'A#', 'B', 'C', 'C#', 'D', 'D#', 'E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B', 'C', 'C#', 'D', 'D#', 'E', 'F', 'F#', 'G']
['B', 'C', 'C#', 'D', 'D#', 'E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B', 'C', 'C#', 'D', 'D#', 'E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B']
['E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B', 'C', 'C#', 'D', 'D#', 'E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B', 'C', 'C#', 'D', 'D#', 'E']
```

# QJewels

Jewels game in SuperBASIC for SMSQ/E (QL derivatives) in High Colour.

Created using EasyPtr and the Turbo compiler

# To build:

- LRUN prepare_bas
- LOAD jewels_bas
- CHARGE


# Jewels

Introduction

QJewels is a game for High-Colour, Hi-Res SMSQ/E systems like QPC or QXL under SMSQ/E. 

QJewels was built using some of the most excellent and free development tools for the QL around, thanks for them, guys - in no particular order:

- SMSQ/E and QPC 
- Turbo
- EasyPtr
- pngCnv
- sox
- uconfig
- and whatever else I've used and forgotten
 
# How to play

Now to the program:

If you've never seen any of the *jewel* programs before (very unlikely if you've ever seen a computer, mobile phone or *pad), the object of the game is to remove as much tiles as you can by bringing at least three of them in line (either horizontally or vertically) by changing places with one of the neighboring tiles (above, below, left, right, but not diagonal).

Just pick the tile that you want to move with the pointer (HIT). The pointer will change to the moving tile sprite. 

Move that sprite (at most one square) away and simply drop it on the tile you want to exchange it with. If you're making at least three in a row, QJewels will remove the row, the other tiles fall down to fill the empty spaces. The top is being refilled with new, random tiles. (This is all much harder to explain than actually done).

This is all shown with some rather nice (I hope) animated sprites. If you have sound enabled and SSS (the sampled sound system) installed, you'll also hear some more or less interesting sound.

You gain a score from removing jewels, initially 1 per removed tile. if after the initial fall-down there's more to remove (because fallen-down pieces make up a new row of at least three), the score you get is doubled, the third time around counts 3 per removed tile, and so forth. There's no high-score table, we're all adult people, aren't we, and don't need such childish features.....?

Should you get stuck on the "where's my next move again" question, press the "Hint" button. This will flag the next possible move the program has detected (which will NOT necessarily be the best one, though). Because nothing is for free in life (except this game) you get a penalty on your score each time you need a hint. QJewels checks after each move done for you if there is another possible move - as long as it doesn't show its final "no more moves" dialog there definitely is a move you could make - you just didn't search hard enough.

# Installation

Installation is very simple: Just extract all the files into one single directory. The sound files are found by using HOME_DIR$, so make sure they end up in the same place as the _exe (You might want to put the sound into a sub-directory of the program directory. In this case you need to configure the files with the sub-directory prefixed, see below).

QJewels incorporates a config level 2 block and can be configured using TT's menuconfig. The following items are configurable:

- large or small jewels (note you need a minimum screen  estate of 480x480 for the "large sprite" option)
- sound on/off
- names of soundfiles played

I'm no particular expert in choosing (or even making) sounds - and I guess someone out there will be much better at that, so I have given you the chance to adapt them to your own liking. There is tons of free gurps, blurps and beeps out there on the internet so go ahead and get you some (The sound files should be re-sampled using sox to 20kHz stereo _ub format). If you change the soundfiles from the original ones, simply supply the name to menuconfig and put the new files into the program directory. If you changed the files and fail to hear anything, although sound is switched on, the program has failed to find at least one of them (it silently falls back to silence...).

Note QPC2 needs to have an "LRESPR xxx_sound_cde command somewhere in your boot file in order to install SSS.

# License
QJewels is supplied in the hope that someone finds it nice, useful (I doubt that) or at least entertaining (I myself have already wasted a lot of time with it. Once it got at least partially playable, it became harder and harder to concentrate on finishing the program instead of playing "just one more round"). 

It's public domain and you can do whatever you like with it. You might even claim it's yours, if you think you need to. I only have a few requirements if you use and distribute the program:

1. Please don't remove this README
2. If you make it available to someone, please make it available to everyone who wants it. Don't put it in closed program libraries.
3. If you think you'd like me to produce some more like this,  please give me feedback (praise, improvement proposals, criticism, payment ;), everything is welcome). 
4. Don't try to complain to me about any time wasted through this game ;)

//==============================================================================
// Contact Info
//==============================================================================
https://www.youtube.com/user/dandymcgee
https://github.com/dbechrd
https://twitter.com/dbechrd
dandymcgee#2568 on Discord

//==============================================================================
// Contents
//==============================================================================
HRTF_MHR_with_demos.zip/
    demos/IRC_1***.wav    Demo files (see below)
    mhr/*.mhr             MHR files (see below)
    alsoft.ini            The OpenAL config file described in the original post
                          (needs to go in your %appdata% folder)
    reddit_post.html      A copy of the original Reddit post for posterity

//==============================================================================
// Purpose
//==============================================================================
This archive contains a few helpful files that allow you to enable HRTF 3D
audio for any game using a sufficiently up-to-date version of OpenAL. It is
based on the following post:
https://www.reddit.com/r/oculus/comments/1fzonq/psa_for_games_using_openal_including_minecraft/

//==============================================================================
// Glossary
//==============================================================================
HRIR = Head-related impulse response

    This data describes the impulses that reach a particular individual's
    eardrums after bouncing off the various parts of their ear.

HRTF = Head-related transform function

    This data describes a transformation function that can be applies to raw
    audio data in order to simulate it having gone through all of the same
    transformations it would have undergone if going into the ear of the person
    whose HRIR data was used to generate the HRTF function. Essentially, this is
    what everything would sound like if you literally traded ears with them.

//==============================================================================
// Usage
//==============================================================================
HRIR data is highly personalized data. How sound interacts with the human body,
head and ears is different in every human. The purpose of the demo files is to
allow you to listen to a bunch of different datasets quickly and try to find
one that most closely matches your own physiology. It's worth noting that it's
possible to have your own head and ears measured in professional studio
environment to produce HRIR data, which can then be converted into an MHR
file perfectly suited for you, but unforuntately this is not a widely accessible
service. If you're lucky enough to have a friend with access to an anechoic
chamber, then I envy you!

You must use headphones to listen to the demos, in-ear "ear buds" are well-
suited for this task, but any high quality headphones will do. I used studio
monitor headphones (Sony MDR7506 Pro) while testing this data. They're about
$90.00 USD on Amazon and the best headphones money can buy for any audio work.

The demos are all the exact same audio test set up: You are seated in the
center of a room and there is a sound rotating around your head, starting
directly behind you, and moving counter-clockwise for a single rotation. The
sound should seem as though it's coming from a perfectly level plane as it
rotates around your head.

Depending on which demo you listen to, it may sound like the source of sound
is moving up or down (i.e. above or below your head, relative to level) as it
rotates around you. If you notice this happening, it means the person this
demo was modeled after had substantially different phsyiology than you. You
should *not* use the corresponding for this demo. The goal is to find the demo
where you notice the least up/down movement; if you get lucky, none at all.

Once you find the demo most well-suited to your hearing, simply take note of
the four-digit number (e.g. 1004 in "IRC_1004_P345.wav"), then find the
corresponding *.mhr file in the mhr/ directory ("oalsoft_hrtf_44100_1004.mhr"
in my case).

The two MHR files called "default-44100.mhr" and "default-48000.mhr" are the
two default functions provided with OpenAL. There are no demo files associated
with them, but you're free to try them out and see how they sound in your game
of choice.

Good luck!
- Dan Bechard

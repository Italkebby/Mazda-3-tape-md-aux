# Mazda-3-tape-md-aux
Trying to achieve aux on my car, with bluetooth connection... I don't know what will happen.
Dislaimer: I don't assume any responsabilities about all this stuff

By the way I'm going to summarize down here all info I found:

First I found a discussion on rx8club.com [link](https://www.rx8club.com/new-member-forum-197/%2415-aux-solution-tape-md-button-262520/) about developing a system DIY (check [Thank all of you](Thanks%20to%20and%20start%20point.png) ). 
So I get the code (in Aux_1_1) and I modify a delay from 1700 to 1750 (check in the code).

Then I decided to draw a schema about all the parts and how to connect them.

![Alt text](schema%20di%20principioV3.drawio.png)

Differently from people in the forum, I decided to grab +12V from cigarette lighter socket because:
- 3/4 pin from Tape connector give always 12v also without key inserts into car. I don't want the system draw current when the car is off
- 11 pin from Tape connector, I don't know why but, with the multimeter it supply only 3v, maybe cause the car was off when I tested.

I think the DCDC converter is a plus it doesn't really required, I could use Vin to supply Arduino with 12V

After I purchased the Bluetooth module [like this one](btmodule.jpg), I was having alternator whine noise in the audio line, this issue could be about ground loop problem so I bought [this](groundloopinsulator.jpg) to detach the ground fixing the problem.


Other info about this project:
- https://github.com/Krasutski/mazda_tape_deck_emulator -> code for Mazda 6 2005 3.0L with tape/md button
- https://nikosapi.org/hardware/mazda-radio/davidoshea-archive/radio/ -> how does it work the bus communication (head unit <--> Tape Deck)
- https://github.com/pschatzmann/ESP32-A2DP -> by using ESP32 and BLE with the smartphone




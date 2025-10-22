# useful settings for TS-590 with hamlib
# *REMEMBER :   parameter in UPLETTER ...must be in UPLETTER!
# 
# If you wish to 
#
#
# I use the tcp connection -m2 to rigctld 
# rigctld is started with

rigctld -m 2037 -r /dev/ttyUSB0 -s 115200 -vvv
# for 5090SG
rigctld -m 2037 -r /dev/ttyUSB0 -s 115200 -vvv
# for 5090SG

# then i use cqrlog and wsjt-x simultanously



# Here are some commands to switch ... e.g. with cqrlog on custom buttons
# set commands are in upletter, read commands in downletter

# comp on/off
rigctl -m2 U COMP 1
rigctl -m2 U COMP 0

# set AF very low
rigctl -m2 L AF 0.1

# when i use FT8 ... very useful
# combined with \ (backslash):
rigctl -m2 U COMP 1\L AF 0.1


###   Tuner
##   off
rigctl -m2 U TUNER 0
##   on
rigctl -m2 U TUNER 1
##   tuning
rigctl -m2 G TUNE


# changing to fm

# and closing squelch (0-1 .... 0.1 ... 0.5 ... 0.9  -on my site also komma possible- 0,1 ... 0,5 ... 0,9  )
rigctl -m 2 L SQL 0.9


# Up Down
rigctl -m2 G UP
rigctl -m2 G DOWN


# set XIT (Hz)
rigctl -m2 Z 50
rigctl -m2 Z 100
rigctl -m2 Z 0
# ...when using wsjt-x with audio frequency below 200 Hz 

# set antenna
rigctl -m2 Y 1
rigctl -m2 Y 2

# switching to memory channel 80
rigctl  -m2 E 80



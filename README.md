# Fright-Farm-Projects

I helped write the code for several projects for Fright Farm 2021 (a haunted attraction).



hayride attractions:

(1) Fire Barn - a barn with four stations on either side that shoot fire into the air (with propane) corresponding to the music
	-for Processing
	-BeatWrite is the main program, BeatListener is a class used by BeatWrite, and Fire.mp3 is the song used
	-senses the wagon (with a debounce), plays the song, and sets off fires timed to different types of sounds detected in the song (e.g., snare or hat)
	-works in general for any song
	-also displays the activity on the screen and includes various delays to account for wagon timing

(2) Spinning Tunnel Barn - a barn with an entrance door, a giant (disorienting) spinning tunnel that surrounds the wagon, and music
	-for Arduino
	-Original only controls the music whereas New with Entrance Door controls both the music and the entrance door (which operates via air compression)
	-basic outline of timing (with delays between each step): activate trip 1 (with a debounce) -> open door -> activate trip 2 (with a debounce) -> close door and play music
	-also deactivates the trips when appropriate to account for back tires

(3) Church Scene - a scene with music and alternating floodlights timed to the music
	-for Arduino
	-senses the wagon (with a debounce), plays the song, and sets off four floodlights (with two controlled per pin) timed to the music
	-timing is specialized to the particular song used



festival area:

Festival Ticket Sign - a large counter to let customers know when to board the hayride
	-for Arduino
	-receives input from a remote control and increments the sign (up or down) via writing to the LEDs on the board
	-uses a 2d matrix to track what each digit looks like

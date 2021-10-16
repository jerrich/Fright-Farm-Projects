# Fright-Farm-Projects
I helped write the code for several projects for Fright Farm 2021 (a haunted attraction).<br />
<br />
<br />
hayride attractions:<br />
<br />
(1) Fire Barn - a barn with four stations on either side that shoot fire into the air (with propane) at certain times corresponding to the music<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-for Processing<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-BeatWrite is the main program, BeatListener is a class used by BeatWrite, and Fire.mp3 is the song used<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-senses the wagon (with a debounce), plays the song, and sets off fires timed to different types of sounds detected in the song (e.g., snare or hat)<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-works in general for any song<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-also displays the activity on the screen and includes various delays to account for wagon timing<br />
<br />
(2) Spinning Tunnel Barn - a barn with an entrance door, a giant (disorienting) spinning tunnel that surrounds the wagon, and music<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-for Arduino<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-Original only controls the music whereas New with Entrance Door controls both the music and the entrance door (which operates via air compression)<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-basic outline of timing (with delays between each step): activate trip 1 (with a debounce) -> open door -> activate trip 2 (with a debounce) -> close door and play music<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-also deactivates the trips when appropriate to account for back tires<br />
<br />
(3) Church Scene - a scene with music and alternating floodlights timed to the music<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-for Arduino<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-senses the wagon (with a debounce), plays the song, and sets off four floodlights (with two controlled per pin) timed to the music<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-timing is specialized to the particular song used<br />
<br />
<br />
festival area:<br />
<br />
Festival Ticket Sign - a large counter board to let customers know when to get on the hayride<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-for Arduino<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-receives input from a remote control and increments the sign (up or down, between 00 and 99) via writing to the LEDs on the board<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-uses a 2d matrix to track what each digit looks like<br />

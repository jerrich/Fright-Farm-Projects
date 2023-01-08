# Fright-Farm-Projects
I helped write the code for several projects for Fright Farm (a haunted attraction) in 2021 and 2022.<br />
<br />
<br />

## 2021

### hayride
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
(4) Traffic Light - a red/green traffic light at the beginning of the hayride to direct the drivers when to depart<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-for Arduino<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-provides an interface (with a button and a screen) to set the planned time span between wagon departures<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-uses a 2d matrix to track what each digit looks like and uses multiplexing to display digits to different parts of the screen<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-order: sets light green -> senses a wagon (with a debounce) -> sets light red for specified time span<br />
<br />
<br />

### festival area
<br />
Festival Ticket Sign - a large counter board to let customers know when to get on the hayride<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-for Arduino<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-receives input from a remote control and increments the sign (up or down, between 00 and 99) via writing to the LEDs on the board<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-uses a 2d matrix to track what each digit looks like<br />
<br />
<br />

## 2022

### haunted house
<br />
(1) Spark Fuse Box - a fuse box with a lever that sparks and pops any time a customer pulls or pushes the lever<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-for Arduino<br />
<br />
(2) Three Sound Button - a button for actors that plays one of three sounds, rotating between them<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-for Arduino<br />
<br />
<br />

### festival area
<br />
Target Game - a carnival game in which two players compete against each other to shoot lit-up targets with pellet guns<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-for Arduino<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-each player has four designated targets that can light up; upon shooting the lit target, the player gains a point and a new target (possibly the same one) lights up<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-writes scores to a scoreboard by shifting numbers out to a series of seven segment displays<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-plays music during the game, announces the winner at the end, and waits for a restart from the employee's button<br />
	&nbsp;&nbsp;&nbsp;&nbsp;-a new random sequence of planned target lighting is assigned for each game; same for each player

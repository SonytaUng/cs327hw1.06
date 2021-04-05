Group menmber: Derrick Wright  dwright@iastate.edu
               Hamza Shahid    hmshahid@iastate.edu
               Sonyta Ung      ung@iastate.edu
The process to achieve this dungeon fog of war and porting to c++ are:
- converting (porting) entire game into C++.
- rename all of your C files with a .cpp extension.
- do a make clobber and update your makefile.
- change structs to classes; this includes the dungeon and the character
structures.
- The dungeon is now dark. we treat the PC as if it is carrying a light with a light 
5x5 region of the dungeon centered on the PC will be illuminated.
- Add support to display the dungeon without the fog of war. 
- create toggle:
	+ 'f'key: togglable effect (you turn it on, and later turn it off again) or a one turn
		  effect (you display the fog-free dungeon, and after you make a move you display the foggy dungeon).
	+ 'g'key: activate teleport mode. When in teleport mode,
		  the movement keys (same as for moving the PC) will move a targeting pointer (for instance, *). A
		  second g will then send the PC to the targeted location. 
	+ 'g'+ 'r'key :  g followed by r (while in targeting mode) will send the PC to a random location.



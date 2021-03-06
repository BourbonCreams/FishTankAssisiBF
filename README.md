# FishTankAssisiBF

This is a guide to the use of the Python script called "script.blend", which is run in Blender. It is meant to replicate possible situations found during the AssisiBF project, which studies the behaviour of real fish and bees when robotic counter-parts are put in the same environment. To know more about AssisiBF, please visit their website: http://assisi-project.eu/

The script uses models of a real fish, a robotic fish and a fish tank, which are located in the 'Models' folder.

The user can change a few settings by editing the 'settings.txt' file, located in the same folder as this file and the script. The user is required to specify a number of real fish and a number of robotic fish that will appear in the scene, as well as their initial, intermediate and final positions. To avoid errors, the user is required to insert the positions in a specific format, here described.
The first line after the two lines that define the number of fish should be a line with the text "Starting positions" followed by the initial positions of the robotic fish first and the real fish then. Following the last position of this list, there must be an empty line. From now on, every time a new set of positions is needed, a line with the text "Inter" should be placed right after the set of positions, which must contain the same number of positions as the previous sets(indeed, this is equal to the sum of the robotic fish and the real fish). The order of these positions is the same as the previous sets and changing it means assigning positions to the wrong fish.

The format of a position is just as important. One space between two coordinates, no letters, no commas(a point is used for decimal numbers). To keep the fish inside of the aquarium, the user is required to set each position within a specific range of values. The corners of the aquarium are the following:

	Corner SW: -25 -24 4.0672
	Corner SE:  17 -24 4.0672
	Corner NE:  17  20 4.0672
	Corner NW: -25  20 4.0672

This means that the x coordinate has a range of [-25; 17] and the y coordinate has a range of [-24; 20]. Coordinates outside these ranges will still be accepted and even though the user will be notified with a message on the Console, the fish will still swim outside the aquarium. Note that the z coordinate should always be 4.067. The height at which the fish swim is not relevant to the project and that value makes the fish stay at the right height.

The following is a working example of the 'settings.txt' file, which defines the creation of 3 fish, a robotic one and two real ones, and three positions for each one of them:



Number of Fish-CASU: 1

Number of zebra-fish: 2


Starting positions

15 13 4.0672

5 20 4.0672

5 22 4.0672



Inter

10 15 4.0672

5 15 4.0672

5 18 4.0672



Inter

8 20 4.0672

5 10 4.0672

5 12 4.0672



*Note that the last 'Inter' position corresponds to the final position.*


#### ANIMATION:

To render the animation, click on the 'Animation' button on the bottom-right panel (it may take some minutes, depending on how many objects are in the scene). The video will appear in the 'Animations' folder. Its name must be changed to make the video playable: '.dvd' must be replaced with '.mpeg'.
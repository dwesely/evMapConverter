# evMapConverter
Stand-alone converter of MU* room information from ASCII format to Evennia batch commands.

The impetus for this project is the following comment in the Evennia repository:
https://github.com/evennia/evennia/pull/1019#issue-172683783

The use case I have in mind is this:

- The designer starts with an idea/sketch of a single scene like a D&D [One Page Dungeon](http://www.dungeoncontest.com/)
- The designer makes a text file in a similar format to the example below (using plain old text editor or something more full-featured like [JavE](http://jave.de/))
- The designer runs the parser, which outputs a batch script to create the scene as described
- The designer looks through the batch script, tweaks it as necessary for their needs
- The designer can run (or share) their batch script as needed

Parsing a map straight into the game seems like it would be a bit error-prone, so this would keep the parsing step offline. Also, the parser wouldn't need to change when the default values change for each scene/setting.  The user can have access to some defaults through the map input format, and the scene/setting details can stay separate from the parser function. The output of the parser would be the batch script to create the scene, with some placeholders to fill in blanks. The user would correct the output for the scene they are creating, not necessarily change the parser to match the setting.

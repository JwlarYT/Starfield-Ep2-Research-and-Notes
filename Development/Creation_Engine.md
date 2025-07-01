Why time skipping is hard:
The Creation Engine tracks the state of the world through modular systems (Actors, AI Packages, markers, etc), many of which are calculated individually and timed to wait for other systems which in turn wait for other systems.

It is possible to just set the time to the next day, but the problem is that doing so does not simultaneously update all those bits and pieces that wait on each other. The incremental time jumps allow everything to catch up, so they remain in the right place.
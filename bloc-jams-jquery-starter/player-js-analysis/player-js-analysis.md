1. This file declares a class, `Player`, instantiates it, and assigns it to a global `player` variable.
2. The `Player` class contains four methods:
    - `constructor()`
    - `playPause()`
    - `skipTo()`
    - `setVolume()`
3. The `constructor()` method sets initial values for the `currentlyPlaying`, `playState`, `volume`, and `soundObject` properties.
    - `currentlyPlaying` is set to the first item in `album.songs`.
    -  The initial `playState` is `"stopped"`.
    -  The `volume` is set to the number `80`.
    -  The `soundObject` instantiates a new `buzz.sound` object using the `soundFileUrl` property of `this.currentlyPlaying`. The `buzz` variable doesn't appear to be initialized here, so presumably it's a dependency loaded elsewhere.
4. The getDuration() method returns this.soundObject.getDuration(). It appears to be a wrapper for a method available on this.soundObject.
5. The getTime() method returns this.soundObject.getTime(). It also appears to be a wrapper for a method available on this.soundObject.



6. The `playPause()` method accepts one parameter, `song`. It sets it to `this.currentlyPlaying` by default. It checks to see if `this.currentlyPlaying` is different from `song`, and if so, it:
    - Stops the `soundObject` property.
    - Removes the `"playing"` and `"paused"` classes from the `element` property of `this.currentlyPlaying`.
    - Sets `this.currentlyPlaying` to the function's parameter, `song`.
    - Changes the `playState` property to `"stopped"`.
    - Instantiates a new sound object using `this.currentlyPlaying`, which was just updated to `song`.
  Then it checks to see if the 'playState' is set to 'paused' or 'stopped'. if it is:
    - sets the sound volume to 'this.volume
    - plays the 'soundObject" property'
    - sets the playState to 'playing'
    - removes the paused class and replaces it with playing
  if neither of these conditions is satisfied:
    - it pauses the soundObject property
    -sets the playState to paused
    - removes classes playing and adds class paused

7. the skipTO method accepts one parameter 'percent'.  then it checks to if the playstate is currently not playing. if so, it returns. otherwise  sets the soundObject to a set time of the percent /100 multiplied by the function getDuration.

8. the setVolume method accepts one parameter, percent.it sets the volume to this value. then it runs the setVolume function

9. finally, the file declares a contructor, player, and sets it to a new user defined value that follows the class Player

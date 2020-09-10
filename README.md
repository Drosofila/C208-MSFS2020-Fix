# C208-MSFS2020-Fix
Improvements to the Caravan engine performance in MSFS2020

As you have probably noticed, the C208 in the new msfs 2020 has some problems regarding the engine behavior and performance. My RL flying experience is limited to small single engine piston aircraft, but I have made some research and talked to people who are real life Caravan pilots and here are some of the problems I found:

The engine performance is way under what it should be, most visible during the take off and when trying to maintain level flight during cruise.

The startup sequence isn't very accurate, but this seems to be a problem in all turboprop aircraft in msfs 2020.

The condition lever isn't well simulated and is tagged as "mixture".

The fuel consumption is wrong. The actual fuel consumption of the plane isn't that far off what it should be, but since the engine is underpowered, you have to input more torque at cruise to keep the indicated airspeed. When checking the tables available in the POH I found that in my cruise settings I was supposed to keep the maximum torque of ~1650 lbs/ft to maintain the indicated airspeed around 140 kt. If I tried to use this power configuration the plane would lose speed and stall. So, to keep the airspeed the way it should be, I had to input around 2100 lbs/ft of torque. This led to a higher fuel consumption.

The ITT is wrong. It doesn't go as high as it should by the book, so it doesn't limit the maximum torque output.

This is what I could do so far:

Changelog v0.3.1:

- Idle power tuned, the plane now shouldn't start mmoving so easily when you release the brakes.
- Engine power tuned.
- Fuel consumption tuned.
- Flight Model tuned.
- Now when you start a flight with the plane in the "cold and dark" state the condition lever is in the CUTOFF position intead of the HIGH IDLE position.
- When you start the flight with the plane in "cold and dark" the propeller is feathered* (read note below) as it should be, but instead of slowly moving to the right angle during engine start as the oil pressure builds up, it just moves when you move the prop lever to max before start, even when the engine is off (this is a problem that will try to solve later, but it might require some custom coding to work the way it should).
- Increased the range that the prop lever control the prop rpm in an attempt to get it to feather, now you can reduce it to around 200 RPM. This is still a work in progress.
- Got the reverse thrust working. It might be overpowered or underpowered though, I'll adjust it in the next updates, but now it works :-).

* The prop still won't feather. I can get it to move to an angle that is close to what the feather angle should be but it still doesn't feather, the only thing you can do is reduce a lot the RPM. I'll keep trying to improve this.
Some other things to keep in mind:
- The beta range (before the reverse) doesn't really do anything now.
- Fuel consumption and climb/cruise power seem to be working the way they should according to the POH I use as reference, but if you notice any abnormalities or bugs please feel free to open an issue or contact me.

Changelog v0.3:

- Engine performance tuned.
- Fuel consumption tuned.
- Flight model changes: I tried to tweak the flight model to increase the drag generated from the flaps, mainly when using full flaps.
- Corrected Ng values at idle power with condition lever at high idle and low idle.
- Stall speeds corrected.
- Propeller angles corrected in the engines.cfg file but the propeller won't feather at all.
- Now you can install it the right way via the "Community" folder (I think it's working).


Changelog v0.2:

- Climb/cruise speeds corrected.
- Elevator trim actuation is now much more smooth than it was before.
- Engine Power tuned (the plane might feel a little overpowered, but I'm still fine tuning the power output).
- Fuel consumption tuned (now it's closer to what it should be, I'll try to improve it).
- AP FD GA angle reduced.
- Idle Ng corrected.

Changelog v0.1:

- Improved the Ng% -> Torque ratio so it delivers more torque with less Ng%, which resulted in a small gain of performance.

- Improved the Fuel Flow of the aircraft. I'm still doing test flights and as of now it consumes around 100 lbs of fuel less than it should in a flight as per the tables available in the POH. Will try to improve this.

- With this mod, I was able to make a flight following the power settings available in the POH and had a performance close to what it should be. I was able to keep the torque within the limits of the POH while maintaining the desired cruise airspeed. The ITT is still lower than it should be (it doens't limit your torque, you actually can go all the way up to around 2000 lbs/ft of torque and keep the ITT in the green, which shouldn't happen according to the POH).

To view the change log and the features in the latest version please check "releases" on the github repository:

https://github.com/Dros0phila/C208-MSFS2020-Fix

There are probably a lot of other problems with this aircraft, but these are the ones I found more relevant as of now. Again, I am no expert in this kind of plane and I might be wrong in some of these findings. I'm also not a programmer and therefore my skills with software are VERY limited. So I'm open to any feedback from actual Caravan pilots, people who know how to code and of course, flight simmers who could enjoy a more realistic Caravan!

Feel free to reach out to me via discord if you have any suggestions: Drosophila#3435

-------------------- INSTALLATION -----------------------

Copy the folder "C208B-mod" to your community folder. 

If you're using Gamepass/Windows Store the path should be:
C:\Users\YourUsername\AppData\Local\Packages\Microsoft.FlightSimulator_8wekyb3d8bbwe\LocalCache\Packages\Community

For the Steam version I'm not sure but it should be something like:
C:\Users\YourUsename\AppData\Local\Packages\Microsoft.FlightDashboard_8wekyb3d8bbwe\LocalCache\Packages\Community

Done! If you have any problems or if you just didn't like the way the plane behaves with this mod you can simply delete this file from the "Community" folder.

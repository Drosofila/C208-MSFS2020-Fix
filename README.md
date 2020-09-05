# C208-MSFS2020-Fix
Improvements to the Caravan engine performance in MSFS2020

As you have probably noticed, the C208 in the new msfs 2020 has some problems regarding the engine behavior and performance. My RL fying experience is limited to small single engine piston aircraft, but I have made some research and talked to friends who are real life Caravan pilots and here are some of the problems I found:
1 - The engine performance is way under what it should be, most visible during the take off and trying to maintain level flight during cruise.
2 - The startup sequence isn't very accurate, but this seems to be a problem in all turboprop aircraft in msfs 2020.
3 - The condition lever isn't well simulated and tagged as "mixture".
4 - The fuel consumption is wrong. The actual fuel consumption of the plane isn't that far off what it should be, but since the engine is underpowered, you ahve to input more torque at cruise to keep the indicated airspeed. When checking the tables avaiable in the POH I found that in my cruise settings I was supposed to keep the maximum torque of ~1650 lbs/ft to maintain the indicated airspeed around 140 kt. If I tryed to use this power configuration the plane would lose speed and stall. So, to keep the airspeed the way it should be, I had to input around 2100 lbs/ft of torque. This led to a higher fuel consumption.
5 - The ITT is wrong. It doens't go as high as it should by the book, limiting the maximum torque output.

This is what I could do so far:

- Improved the Ng - Torque ratio so it delivers more torque with less Ng, which resulted in a gain of performance.
- Improved the Fuel Flow of the aircraft. I'm still doing test flights and as of now it consumes around 100 lbs of fuel less than it should in a flight as per the tables avaiable in the POH. Will try to improve this.
- With this mod, I was able to make a flight following the power settings avaiable in the POH and had a performance close to what it should be. I was able to keep the torque within the limits of the POH while maintaining the desired cruise airspeed. The ITT is still lower than it should (it doens't limit your torque, you actually can go all the way up to around 2000 lbs/ft of torque and keep ITT in the green, which woulndn't happen according to the POH).

There are propably a lot of other problems with this aircraft, but these are the ones I found more relevant as of now. Again, I am no expert in this kind of plane and I might be wrong in some of these findings. I'm also not a programmer and therefore my skills with software are VERY limited. So I'm open to any feedback from actual Caravan pilots, people who know how to code and of course, flight simmers who could enjoy a more realistic Caravan!

Feel free to reach out to me via discord/e-mail.

-------------------- INSTALLATION -----------------------

1. Make a backup of the engines.cfg and target_performance.cfg in the folder C:\Users\YourUsername\AppData\Local\Packages\Microsoft.FlightSimulator_8wekyb3d8bbwe\LocalCache\Packages\Official\OneStore\asobo-aircraft-208b-grand-caravan-ex\SimObjects\Airplanes\Asobo_208B_GRAND_CARAVAN_EX
(I believe that for the Steam users the FlightSimulator_xxxxxx folder should be in your steam games library folder)

2. Copy the provided engines.cfg and target_performance.cfg in the same folder.

Done! If you have any problems or if you just didn't like the way the engine behaves with this mod you can simply delete this two files and copy your backups back to this folder.

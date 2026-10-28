# SLUDGE LIFE VR - tester build 0.9.23

the spray can recharges much faster now. let go of the trigger and give it a couple quick shakes. hold left grip while moving to run. item/climbing grabs, laptop precision and tool chords keep priority. crouch is on the left trigger, jump is still right A. keep the left grip released for crouch; grip + trigger still does vandal eyes. right B toggles the camera now and the shoulder grab still works.

alrightY, here's SLUDGE LIFE 1 in VR. i wanted it to feel like you're actually Ghost: green hands, black biker gloves, black nails, the ant tattoo, and a bunch of stuff you can mess with physically.

you can climb with the spray can in your right hand now. grip the ladder and pull like normal, then keep your left grip on the ladder while you let go with the right and paint with the right trigger. release both grips to drop.

this is a test build. go play, try the weird shit, and tell me what feels wrong. the rocket red-button touch target is on the actual red cap now. the old low D, G, A and B acid-bass sounds are back with more distortion and bit-crushing. they ring for about 2.8 seconds. the kick still hits louder. the kick is still a short dirty thud. the last build's frame-drop fixes are still in here. the club mpc, slow button pokes, and proper spray-can sounds are included. you gotta shake the can every so often now too. the full laptop screen, animated slugs and middle-finger shortcut are included. those still need more headset testing.

## get it running

you need your own installed Windows Steam copy of **SLUDGE LIFE**, a PC VR headset, motion controllers, and SteamVR. my setup is Quest 3 + Virtual Desktop + SteamVR. other setups haven't been checked. this isn't a standalone Quest install.

1. close the game and extract this whole ZIP somewhere you can keep it. don't run it from inside the ZIP.
2. run **INSTALL.cmd**. it looks for the game in your Steam libraries. if it can't find it, paste the folder containing **SludgeLife.exe**. BepInEx and the required runtime are included.
3. connect the headset to your PC and start SteamVR. make sure SteamVR sees the headset and both controllers.
4. keep Steam open, then run **LAUNCH-VR.cmd** from this extracted folder. use this launcher for the VR arguments.

if it picked the wrong drive or you've got a custom install, open a terminal in this folder and use:

```bat
INSTALL.cmd -GamePath "D:\SteamLibrary\steamapps\common\Sludge Life"
LAUNCH-VR.cmd -GamePath "D:\SteamLibrary\steamapps\common\Sludge Life"
```

SL1 has no native Run query in its movement FSM; the shared left-grip binding does not add a speed multiplier here. Sludge Life 1 needs a small, hash-checked OpenVR settings patch. The installer backs up the original and refuses an unrecognized game build before installing anything. If it refuses yours, send me the Steam build number.

the installer keeps backups of files it replaces. it doesn't touch your save. an existing different mod loader makes it stop instead of stomping over it. a clean game/mod setup is the easiest first test.

## how the controls are lined up

| control | what it does |
|---|---|
| left stick | move, based on where you're looking |
| right stick | smooth turn; moves the cursor when the laptop/menu is open |
| right trigger | talk/use stuff; click on the laptop; hold to drag a window |
| right A | jump; hold it in the air to glide after you've got the glider |
| hold left grip while moving, away from physical holds | sprint/run (Shift); right A can still jump |
| hold left trigger (left grip released) | crouch; press right A at the same time to crouch-jump where the game allows |
| left stick click | fart on the ground, flip in the air when the game lets you |
| right stick click | smoke when the game allows it |
| left Y | pause |
| either grip near food, soda or a disk | grab it; let go to drop it |
| grip a ladder/climb area and pull | physical climbing, including with the spray can out; release both grips to let go |
| right grip near a basketball | grab it; move your hand and release to shoot |
| right grip behind your right shoulder | pull out the camera once you have it; return it there and release to stow |
| right B | alternate camera toggle |
| right trigger with camera out | take a picture; you can also poke its top shutter |
| left grip supporting the camera | steady it; left stick up/down zooms |
| left grip + X / left grip + trigger | telewarp / Vandal Eyes |

on the laptop, **left grip slows the cursor**, left stick scrolls, and right grip is right-click. there isn't a hand laser. **F10** on the keyboard recenters the view and puts an open menu in front of you.

## actually use your hands

- hold right trigger and physically sweep the can over the tag. after about 7.5 seconds of spraying, release the trigger and shake a few times to mix it, then keep painting. the ball rattles with the rumble and the nozzle hisses while spraying. your tag keeps its progress. the can shows up when the game's spray interaction is active.
- grab a soda or slug and keep gripping while bringing it to your mouth. tilt the soda a little. grabbing it alone doesn't eat it. the slugs should still squirm, and they're meant to stay their big cartoony game size.
- poke buttons and bells with your empty index finger. on the rocket, poke the actual red cap; the invisible target above it was the problem. the first game still uses its normal launch checks. push doors with an empty hand.
- pet the cats and dogs. try scratching under a cat's chin for the purring rumble.
- tap the club MPC pads with your fingers or palm and play drums along with the song. lift between hits. soft taps are louder now, hit harder for full level. the top row is low D2, G2, A2 and B2 acid bass from left to right, with heavier distortion and crunch. they ring for about 2.8 seconds. the kick pads are about 4.6 dB louder. different notes can ring together, and tapping the same note restarts it. the other twelve pads are drums, with a short grimy kick.
- with the glider out, empty hands should grab the metal handles automatically. keep holding right A; steer with the left stick.
- on mushrooms, the left stick flies where you're looking, including up/down. left Y uses the game's return action.

to flip somebody off: hold **left X with the left grip released**, and release the right grip to extend the middle finger. squeeze the grip to lower it. this uses the Quest controller's touch/grip input, not optical finger tracking.

the game's unlocks and story rules still apply. this doesn't give you every item at the start.

## stuff i really want tested

walk around the club and the rest of the map, play the mpc, poke buttons and pet a cat. tell me if the stutters settle down. after 20 seconds of play, hold both grips for a capture if it is still dropping frames; the matching text now includes timing numbers.

check the whole laptop screen, especially the left edge icons, and make sure you can actually click them. hold a slug away from your face and rotate your wrist. drink a soda and check that the drinking animation is the right way up. shake the spray can, then stop and listen for the sound to settle.

try climbing into a tag with the can out, keeping your left grip on the ladder while painting, and grabbing the next hold with the right grip. then try ladders and getting off the top, the glider handles, camera grip/photos, basketball shots, red buttons, food, pets and doors. try normal progress too so we catch anything that messes with the actual game. do some room-scale turning and make sure forward still makes sense.

## if something gets fucked up

tell me **which game/build, headset, connection method, where you were, what you did, and what you expected**. a screenshot and the steps to make it happen again help way more than just "it's broken."

hold **both grips for a second**, or press **F8**, for eye-view captures. they go in `BepInEx/SludgeLifeVR-Captures` inside the game folder. the screenshots won't include SteamVR/Virtual Desktop system overlays. include the matching `.txt` capture report and `BepInEx/LogOutput.log` when you send a bug. **F9** writes a scene report. **F11** toggles VR.

if you're stuck looking at SteamVR's "next up" screen or it launches flat, close the game, check the headset connection in SteamVR, then try **LAUNCH-VR.cmd** again. if it's still busted, send the log.

## change settings or take it out

after the first run, settings are in `BepInEx/config/local.sludgelife.vr.cfg`. close the game before editing. smooth turning defaults to 240 degrees/second. lower that if it's too much, or set `SmoothTurning = false` for snap turning.

to remove this package, close the game and run **UNINSTALL.cmd**. it restores matching original files and removes matching mod files from its install record. it leaves your saves, captures, logs, configs and backups alone. files changed by something else are kept, and the loader is kept if other mods need it.

this is unofficial. you still need to own the game. source is in `Source/`; dependency licenses and source archives are in `THIRD-PARTY/`. now go get weird and let me know what breaks.

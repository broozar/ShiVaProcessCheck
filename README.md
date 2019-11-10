# ShiVaProcessCheck
Plugin for desktop (Win/Mac/Linux) that checks and counts process names

## Possible use cases
- check if OBS or XSplit are running -> possible twitch streamer detected
- check if user is running steam -> suggest other steam games to user
- check which browser is running -> offer specific extensions for download
- detect linux desktop environment by scanning for its signature processes
- etc.

Comes with STE packs for the plugin itself and a demo.

## Code
```
-- returns NIL on failure, otherwise the number of processes with that name
-- process name is case insensitive
local vCount = pscheck.test("chRoMe.eXe")

if vCount == nil then
	log.error ( "PSCheck failed!" )
else
	log.warning ( "Number of processes with the name chrome.exe: " ..vCount )
end
```

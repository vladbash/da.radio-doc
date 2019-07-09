# Task

You need implement a web-application based on attached templates.
Basically you need to implement web aduio player which will work with audio streams.

[Template for task]()

Tasks:
1. You need to implement a state manager, which will store:
    -  tracklist, will being update by two different ways at least (http, socket);
2. Implement socket service:
    - tracklist updating (communicating with store);
    - current playing track updating.
3. Implement service for audio stream reading.
4. Implement hotkeys for player controlling:
    - volume control;
    - hotkey for muting;

All of the tasks must be implemented with using of any JS reactive library. RxJS is recomended for usage, but it isn't required library.
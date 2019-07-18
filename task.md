# Task

You need implement a web-application based on attached templates.
Basically you need to implement web aduio player which will work with audio streams.

References:

- radio stream link: `http://{host}:{port}/radio`
- swagger link: `http://{host}:{port}/swagger`
- socket link: `http://{host}:{port}`
- templates: [Templates for task]()

Tasks:
1. You need to implement a state manager, which will store:
    -  tracklist, will being update by two different ways at least (http, socket) - `/api/playlist` - you can get all of actual tracks by this endpoint.
The list will be updated when somebody likes track. Playlist must be sorted with likes counter.
    ![](http://dl3.joxi.net/drive/2019/07/15/0001/2211/108707/07/6ceebf6fcc.jpg)
2. Implement socket service:
    - tracklist updating (communicating with store) - it is updated when somebody likes. Socket events:
        - `trackUpdated` - is emitted with updated data; 
        - `trackAdded` - when someone adding new track to playlist;
    - current track - Socket events:
        - `currentTrackUpdated` - is emitted with current playing track when track changing or track metadata changing.
3. Implement functionallity for reactive searching in tracks list. 
![](http://dl4.joxi.net/drive/2019/07/15/0001/2211/108707/07/88518c8882.jpg)
When user inputs some text in the field, list must be immediately filtered with keeping positions.
![](http://dl3.joxi.net/drive/2019/07/15/0001/2211/108707/07/6b96453d45.jpg)

4. Implement hotkeys for player controlling:
    - volume control;
    ![](http://dl4.joxi.net/drive/2019/07/15/0001/2211/108707/07/8a08db3208.jpg)
    - hotkey for muting;
![](http://dl3.joxi.net/drive/2019/07/15/0001/2211/108707/07/ce75239e72.jpg)

## Recommendation and requirement
All of the tasks must be implemented using any JS reactive library. RxJS is recommended reactive library but you are free to pick any.
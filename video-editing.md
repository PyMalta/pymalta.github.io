Video editing is HARD, there's too many things can go wrong with encoder, file formats, keyframes, timestamps, etc.
This section aims to help organizers with recording, editing and publishing presentation videos.

## Recording

### Video Recording

We found it best to record with highest possible quality (1080p), beware that still cams may have a restriction on maximum video length, and someone will need to manually click "record" every X minutes (30m/60m/etc).

### Audio Recording

Since the video cam may not have the best mic, and be placed too far from speaker, using an external audio recording device is advised. 

For example, simply place a phone with voice recorder app running placed on table/podium nearby. A wireless headset or body mic is even better if available.

### Screen recording

To avoid messing with slides placement inside the video, we found it best to ask presentor to record his screen while presenting it. With that video we can simply overlay the 2 recordings together and sync them with little effor.

If the presentor doesn't have a screencast / screen recording application installed, instruct to download the open-source [OBS Studio][2], set it to record the display where presentation is running (i.e external monitor / projector), and output to a  recorded file.

## Editing

I used [VideoMeld][1] to edit our first recorded presentation. It's not free, but quite small and features overlaying images or text, multi-tracking, effects, transitions, etc. Other solutions may be possible. Beware that the final rendering may take a long time; in our experrience it can taks at least double the original video length.

## Multiplexing

Often times additional slicing and joining is required. To avoid re-rendering/encoding the whole video for these simple actions, we suggest using [FFmpeg][3] (e.g with [Avidemux GUI][4]) to simply mux the channels.

**NOTE:** do note that these actions normally only slice to timestamps with keyframes in them, so make sure you slice to the keyframe or output will not appear in sync.

[1]: http://videomeld.com/
[2]: https://obsproject.com/
[3]: https://ffmpeg.org/
[4]: http://avidemux.sourceforge.net/download.html

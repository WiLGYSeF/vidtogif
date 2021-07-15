# vidtogif

Create gif summaries of videos by showing video frames every *n* seconds.
Saves the gif files using the same filename with a `.gif` appended.

vidtogif picks the gif framerate and seconds per video frame based on the duration of each video, which can be modified in the script.

Designed to create gifs for batches of videos at a time.
Will skip videos that already have gif summaries.

# Requirements

- ffmpeg
- ffprobe

# Usage

```bash
vidtogif input1.mp4 abc/input2.mp4
```

Creates `input1.mp4.gif` and `abc/input2.mp4.gif`.

---

Creating gifs for all mp4 and mkv files using `find`:
```bash
find \( -name "*.mp4" -or -name "*.mkv" \) -exec vidtogif -vvt {} \+
```

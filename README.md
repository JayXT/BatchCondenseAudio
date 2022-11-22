# BatchCondenseAudio
A bash script for GNU/Linux relying on subs2cia to extract and condense audio for all video files in the current directory.

## Behavior
The script goes over video files in the current directory, extracts and condenses audio from each using subs2cia utility.
The video files type is selected based on first file extension detected: mkv, mp4, or avi.
The subtitles are fetched from: ass files, srt files, or video files.

## Prerequisites
- [subs2cia](https://github.com/dxing97/subs2cia) has to be installed.
- The script should be placed in some directory under the $PATH (in other words user should be able to call it from any directory in the terminal).
- Execution rights have to be granted to the script file.

## Limitations
- All video files for condensing audio should have the same extension.
- If built-in subtitles aren't provided, external subtitles should be present in the same directory.
- External subtitles should have the same extension and their names should match the respective video files.

## Usage
1. Open a terminal in the target directory that contains video files and optionally subtitles files, providing built-in subtitles aren't available.
2. Run batch_condense_audio script.
3. The script will go over all video files with the same extension and will extract and combine audio fragments in accordance with subtitle timing using built-in subtitles (if external ones are missing), or ass files (if one such file is detected), or srt files (if one such file is detected).

If necessary the script can be changed to use a different target subtitle language instead of Japanese. 

Feel free to use the resulting mp3 audio files for passive immersion or any other activities.

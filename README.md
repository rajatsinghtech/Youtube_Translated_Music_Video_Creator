> Written manually, without AI assistance.

# Youtube_Translated_Music_Video_Creator

## What this does

Multi-threaded Python app that downloads a YouTube video and its transcript,
translates the transcript into the language of your choice, and burns it
back onto the video as subtitles â€” making music videos accessible across
languages. Demo video (UTS SharePoint):
https://studentutsedu-my.sharepoint.com/:v:/g/personal/rajat_singh-2_student_uts_edu_au/EeEUQCi8n39Eg1oOdMe2nWgBay4jM8bC0S9SxWwHUl4eqw?e=GozSa7

## Business process

Give it a video URL and a target language; get back the same video with
translated subtitles. Download, transcription, translation, and rendering run
as concurrent stages so long videos don't stall on any single step.

## Technical flow

`main.py` orchestrates; `code/download_yt_video.py` fetches video +
transcript; `code/subtitle_processing.py` translates and times the
subtitles; `code/render.py` burns them in (`constants_values.py` holds the
shared settings, `config.py` the credentials). Finished videos land in
`video/`.

## Repository structure

- [`main.py`](main.py) â€” entry point
- [`config.py`](config.py) â€” API credentials (fill in your own)
- [`code/`](code/) â€” download, subtitle, render, constants modules
- [`video_creator/`](video_creator/) â€” created-video workspace
- [`video/`](video/) â€” rendered output

## How to run

Install the requirements, put your API keys in `config.py`, then run
`main.py` with a video URL and target language.

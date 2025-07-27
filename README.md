# 🎵 Hindi Song Transcription Pipeline using Whisper AI

This project automates the process of separating vocals from Hindi songs and generating accurate `.srt` subtitle files using OpenAI’s Whisper transcription model.

---

## 🧠 Project Overview

The objective of this project is to build a pipeline that:

1. Accepts `.mp3` songs as input.
2. Separates vocals (optional).
3. Converts audio to a suitable format.
4. Transcribes vocals using the Whisper model.
5. Generates `.srt` subtitle files with time-aligned captions.

---

## 🚀 Pipeline Workflow

```mermaid
graph TD
    A[MP3 Songs in /input] --> B[Vocal Separation using Spleeter]
    B --> C[Convert vocals to WAV using ffmpeg]
    C --> D[Transcribe using Whisper (large-v2)]
    D --> E[Generate song_name.srt]

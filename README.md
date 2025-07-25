# Agentic Pipeline for Speaker Diarization and Quality Check

This notebook implements a Python pipeline for generating subtitles from audio files, featuring speaker diarization and a quality check agent. It's useful for analyzing short clips with multiple speakers, producing SRT files with labeled dialogues.

## Features
- Speaker diarization with consistent labeling.
- Dialogue-level transcription.
- Confidence-based quality evaluation per segment.

## Approach
1. **Audio Preparation**: Standardize audio to mono PCM WAV.
2. **Transcription**: Leverage Whisper for accurate segmenting.
3. **Diarization**: Use pyannote embeddings and clustering for speaker assignment—more reliable than basic methods.
4. **Merging**: Combine segments for natural flow.
5. **Output**: SRT with labels.
6. **Quality Agent**: Rule-based confidence scoring and feedback.

## Pipeline Flow
Input audio → Convert → Transcribe → Embed & Cluster → Merge → SRT & Quality Report.

## Limitations and Improvements
- Limitations: Fixed speaker count; best on clean audio.
- Improvements: Add overlap detection; LLM feedback; auto-speaker estimation.

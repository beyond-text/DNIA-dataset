# Disfluent Navigational Instruction Audio (DNIA) Dataset

This is the repository that contains the Disfluent Navigational Instruction Audio (DNIA) dataset from the paper _Beyond Text: Improving LLM’s Decision Making for Robot Navigation via Vocal Cues_ [arXiv](https://arxiv.org/abs/2402.03494).

## Update

* 2024-03-27: We published the initial release of the dataset with 6 curated entries from the full dataset. We are working hard on organizing and preparing the rest of the dataset and will publish the full dataset in the near future. Stay tuned.

## Overview

Disfluent Navigational Instruction Audio (DNIA) dataset is a dataset comprising a diverse collection of human
audio recordings. These recordings capture a spectrum of
navigational disfluencies, including 500 audio clips with a wide array of native and nonnative speaker vocal styles. Each clip, ranging from 10 to
30 seconds, includes a series of English directives necessary for navigating to a specified location. The audio files
are in WAV format, normalized with a headroom of -2dB.

## Get Started

The dataset is located under the [DNIA](./DNIA/) folder of this repository. The [audio](./DNIA/audio/) folder contains all the audio files. The audio files are in `.wav` format. The files are named by `<type>_<number>.wav` where type is either _language uncertainty (LU)_ or _vocal tone uncertainty (VU)_, correspoding to the two types of uncertainties mentioned in the paper.

The dataset comes with the [annotation](./DNIA/annotation.csv) file that documents the information about the dataset. There are the following columns in the file:

* `audio_name`: the filename of the audio file
* `transcription`: the transcription of the audio file, using [Whisper](https://arxiv.org/abs/2212.04356)
* `type`: the type of uncertainty (_language uncertainty (LU)_ or _vocal tone uncertainty (VU)_)
* `choices`: GPT-4 (`gpt-4-1106-preview`) generated choices
* `annotation`: human annotated choice

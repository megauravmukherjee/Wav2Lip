# Wav2Lip
# Lip Sync using Wav2Lip

![Input Video](https://drive.google.com/file/d/1pxut2vyao50gXhhl___x0nG9vnaOrRGU/view?usp=sharing)
![Input Audio](https://drive.google.com/file/d/1JEXKQjpoaiatahNNtRkmshDhi5KnYn6I/view?usp=sharing)
![Output Video](https://drive.google.com/file/d/1Zael0mLGTDifRiispRGb1ZUtJcpNeOFb/view?usp=sharing)

## Introduction

Lip Sync using Wav2Lip is a project that enables the synchronization of audio with video, creating realistic lip movement animations from an audio source and a video clip. This repository provides the code and instructions for achieving lip synchronization using the Wav2Lip pre-trained model.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Variations to Try](#variations-to-try)
- [Evaluation](#evaluation)

## Installation

To get started with Lip Sync using Wav2Lip, follow these installation instructions:

1. Clone the project repository:

   ```bash
   git clone https://github.com/zabique/Wav2Lip.git
   cd Wav2Lip

2. Install the required dependencies:
   pip install -r requirements.txt

3. Download the Wav2Lip pre-trained model:
   wget 'https://iiitaphyd-my.sharepoint.com/personal/radrabha_m_research_iiit_ac_in/_layouts/15/download.aspx?share=EdjI7bZlgApMqsVoEUUXpLsBxqXbn5z8VTmoxp55YNDcIA' -O 'checkpoints/wav2lip_gan.pth'

4. Download the pretrained model for face detection:
   wget "https://www.adrianbulat.com/downloads/python-fan/s3fd-619a316812.pth" -O "face_detection/detection/sfd/s3fd.pth"

## Usage

1. Once you have installed Lip Sync using Wav2Lip and downloaded the necessary models, you can start using it to synchronize audio with video. Here's an example command:
   cd Wav2Lip
   python inference.py --checkpoint_path checkpoints/wav2lip_gan.pth --face "path_to_input_video.mp4" --audio "path_to_input_audio.wav" --nosmooth --pads 0 0 0 0 --resize_factor 1

Replace "path_to_input_video.mp4" with the actual file path to your input video and "path_to_input_audio.wav" with the actual file path to your input audio. The synchronized video will be saved in the Wav2Lip/results/ folder.

## Variations to Try

You can experiment with different variations of the synchronization process:

1. Adjust the padding: You can set the padding using the --pads argument to control the video frame padding.

2. Resize the video: Use the --resize_factor option to reduce the video resolution, which may yield better results for lower resolution videos.

3. Disable smoothing: To prevent over-smoothing of face detections, use the --nosmooth argument.

## Evaluation

Please check the `evaluation/` folder for the instructions.




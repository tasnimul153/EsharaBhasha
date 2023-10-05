# EsharaBhasha: Real-time Bangla Sign Language Translator

## Overview
EsharaBhasha is a real-time translator designed to bridge the communication gap between the speaking and hearing-impaired community of Bangladesh and those who don't understand Bangla sign language. While many apps offer spoken language translations, none cater to translating Bangla sign language. Our solution leverages machine learning and computer vision to make this translation possible.

## Problem Statement
In Bangladesh, a significant number of individuals suffer from speech and hearing impairments. The challenge arises when they interact with those unfamiliar with sign language. Although mobile apps exist for spoken language translations, a dedicated solution for Bangla sign language is absent. EsharaBhasha aims to fill this void.

## How It Works
1. **Gesture Recognition**: Our system uses Google’s MediaPipe Holistic for the initial recognition of holistic landmarks which includes both hands and poses.
2. **Data Collection**: We collect time series key-points of the recognized landmarks and use them to train our LSTM (Long Short-Term Memory) machine learning model. Our dataset boasts over 20 distinct gestures.
3. **Implementation**: Post training, we employ the open-source app framework, Streamlit, to showcase our results.

## Technical Details
- **MediaPipe Holistic**: A powerful tool used for real-time perception of human positioning, which provides a combination of pose landmarks, face landmarks, and hand landmarks. We utilize 33 pose landmarks and 21 hand landmarks per hand for each gesture.
- **Data Collection**: Over 300 videos per gesture class were collected. Each video is split into 30 frames, with key points from each frame saved as NumPy array formatted files.
- **Optimization**: To improve efficiency, we omitted the facial mesh from the key point extraction process since facial expressions aren't crucial for recognizing hand gestures.

## Future Scope
This model paves the way for the development of a smartphone or web application that can act as an interpreter between individuals communicating through sign language and those who don't.

## Paper: 
https://1drv.ms/w/s!Argsykg2L1k6gaACcm67_5Rsp41jDg?e=CV6XUN

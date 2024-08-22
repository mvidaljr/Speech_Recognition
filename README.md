# Speech Recognition with Python

## Project Overview

This project leverages the `speech_recognition` library in Python to convert spoken language into text. The goal is to build a simple and effective speech-to-text system that can be used in various applications such as voice-controlled systems, transcription services, and accessibility tools.

## Tools & Libraries Used

- **Speech Recognition:**
  - `speech_recognition` for capturing and processing audio input.
- **Audio Input:**
  - Supports various audio sources such as microphones or pre-recorded audio files.

## Methodology

### Speech Recognition Process:

1. **Audio Capture:**
   - Captured audio input using a microphone or loaded an audio file.
  
2. **Speech Recognition:**
   - Used the `Recognizer` class from `speech_recognition` to process the audio and convert it into text.
   - Supported multiple recognition engines, such as Google Web Speech API and Sphinx.

### Example Usage:

```python
import speech_recognition as sr

# Initialize the recognizer
r = sr.Recognizer()

# Capture audio from the microphone
with sr.Microphone() as source:
    print("Say something:")
    audio = r.listen(source)

# Recognize speech using Google Web Speech API
try:
    print("You said: " + r.recognize_google(audio))
except sr.UnknownValueError:
    print("Google Speech Recognition could not understand the audio")
except sr.RequestError as e:
    print(f"Could not request results from Google Speech Recognition service; {e}")
```

## Results

The project successfully converted speech to text using the `speech_recognition` library. The system demonstrated robust performance with clear audio and handled various speech patterns effectively.

## Conclusion

This project shows the power and flexibility of the `speech_recognition` library for building speech-to-text applications. The system can be easily integrated into larger applications that require voice interaction.

## Future Work

- Explore other speech recognition engines for improved accuracy and language support.
- Implement noise reduction techniques to improve recognition in noisy environments.
- Develop a real-time application with continuous listening and processing capabilities.

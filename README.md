# finding-sampling-rate-of-audio-recorded.
'''Python script using pydub: Quickly find the sampling rate of an audio file. The code loads the audio file, extracts the frame rate, and prints the sampling rate. Easy and efficient for users needing a rapid sampling rate assessment in a Python environment.
Description: Finding the Sampling Rate of an Audio File in Python

This Python script is designed to determine the sampling rate of an audio file using the pydub library. The sampling rate represents the number of samples of audio carried per second, and it is a crucial parameter for understanding the characteristics of the recorded sound.

The script defines a function named get_sampling_rate, which takes the file path of the audio as input and utilizes the AudioSegment class from pydub to load the audio file. Subsequently, it retrieves the frame rate, which corresponds to the sampling rate of the audio. The result is then printed to the console.

To use the script, replace the placeholder file path with the actual path to your audio file. The pydub library simplifies the process of working with audio files, making it easy to extract essential information such as the sampling rate.

This script offers a straightforward solution for users who need to quickly determine the sampling rate of an audio file within a Python environment.'''
pip install librosa
import librosa

def get_sampling_rate(audio_file_path):
    y, sr = librosa.load(audio_file_path, sr=None)
    return sr

# Example usage
audio_file_path = 'path/to/your/audio/file.wav'
sampling_rate = get_sampling_rate(audio_file_path)
print(f"The sampling rate of the audio is: {sampling_rate} Hz")


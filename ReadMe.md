# Speaker Diarization and Gender Classification

This project performs speaker diarization and gender classification on audio extracted from YouTube videos. The notebook provides functions to download YouTube audio, convert it to WAV format, perform speaker diarization, and classify speakers by gender using pre-trained models.

## Requirements

To run this project, you need the following libraries:

- pydub
- pytube
- pyannote.audio
- transformers
- google.colab

You can install the necessary packages using the following commands:

    pip install pydub
    pip install pytube
    pip install pyannote.audio
    pip install transformers
    pip install google-colab

## Functions

### `download_and_convert_audio(video_url)`

Downloads audio from a YouTube video and converts it to WAV format.

**Parameters:**
- `video_url` (str): The URL of the YouTube video.

**Returns:**
- `str`: The file path of the converted WAV file.

### `perform_speaker_diarization(audio_file_path, hf_token)`

Performs speaker diarization on the provided audio file.

**Parameters:**
- `audio_file_path` (str): The file path of the audio file.
- `hf_token` (str): Hugging Face API token.

**Returns:**
- `int`: Total number of speakers.
- `list`: List of file paths for each speaker's audio segments.

### `classify_speakers(files)`

Classifies the speakers by gender.

**Parameters:**
- `files` (list): List of file paths for each speaker's audio segments.

**Returns:**
- `list`: List of tuples containing file paths and gender classification predictions.

### `process_video(video_url, hf_token)`

Main function to process a YouTube video URL, perform speaker diarization, and classify speakers by gender.

**Parameters:**
- `video_url` (str): The URL of the YouTube video.
- `hf_token` (str): Hugging Face API token.

**Returns:**
- `dict`: Dictionary containing total speakers, male speakers, and female speakers.

## Example Usage

Here's an example of how to use the main function in the notebook:

    if __name__ == "__main__":
        video_url = "https://www.youtube.com/watch?v=RjIxvwHZ3i0"
        hf_token = "your_hugging_face_api_token"  # Replace with your Hugging Face token
        result = process_video(video_url, hf_token)
        print(result)

## Author

This project was developed by Sai Koushik Katakam.

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.

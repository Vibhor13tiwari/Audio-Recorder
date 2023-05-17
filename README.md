# Audio-Recorder
This is a simple audio recording application made on Android studio in java language.
It has three buttons: Record, Play, and Stop. When the Record button is clicked, the MediaRecorder object is created and configured to record audio from the microphone.
The audio is then recorded to a file called "testRecordingFile.mp3" in the device's external storage. 
When the Play button is clicked, the MediaPlayer object is created and configured to play the audio file.
The audio is then played back through the device's speakers. When the Stop button is clicked, the MediaRecorder object is stopped and the MediaPlayer object is released.

The following is a brief explanation of each function in the code:

    isMicrophonePresent() checks to see if the device has a microphone.
    getMicrophonePermission() requests permission to access the microphone.
    getRecordingFilePath() gets the path to the audio file.
    Record() starts recording audio.
    Play() plays back the audio file.
    Stop() stops recording and releases the audio file.

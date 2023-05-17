# Audio-Recorder
This is a simple audio recording application made on Android studio in java language.
It has three buttons: Record, Play, and Stop. When the Record button is clicked, the MediaRecorder object is created and configured to record audio from the microphone.
The audio is then recorded to a file called "testRecordingFile.mp3" in the device's external storage. 
When the Play button is clicked, the MediaPlayer object is created and configured to play the audio file.
The audio is then played back through the device's speakers. When the Stop button is clicked, the MediaRecorder object is stopped and the MediaPlayer object is released.

The following is a brief explanation of each function in the code:

    isMicrophonePresent() checks to see if the device has a microphone by calling the getPackageManager().hasSystemFeature(PackageManager.FEATURE_MICROPHONE) method. If the method returns true, then the device has a microphone. Otherwise, the device does not have a microphone.
    getMicrophonePermission() requests permission to access the microphone by calling the ContextCompat.checkSelfPermission(this, Manifest.permission.RECORD_AUDIO) method. If the method returns PackageManager.PERMISSION_GRANTED, then the app has permission to access the microphone. Otherwise, the app does not have permission to access the microphone and the user will be prompted to grant permission.
    getRecordingFilePath() gets the path to the audio file by creating a ContextWrapper object and then calling the getExternalFilesDir(Environment.DIRECTORY_MUSIC) method on the ContextWrapper object. The getExternalFilesDir() method returns a File object that represents the directory where the app can store its external files. The Environment.DIRECTORY_MUSIC constant represents the directory where the app can store music files.
    Record() starts recording audio by creating a MediaRecorder object and then calling the setAudioSource(), setOutputFormat(), setOutputFile(), and prepare() methods on the MediaRecorder object. The setAudioSource() method specifies the source of the audio to be recorded. The setOutputFormat() method specifies the output format of the audio. The setOutputFile() method specifies the path of the audio file. The prepare() method prepares the MediaRecorder object to start recording.
    Play() plays back the audio file by creating a MediaPlayer object and then calling the setDataSource(), prepare(), and start() methods on the MediaPlayer object. The setDataSource() method specifies the path of the audio file. The prepare() method prepares the MediaPlayer object to start playing. The start() method starts playing the audio file.
    Stop() stops recording and releases the audio file by calling the stop() and release() methods on the MediaRecorder object. The stop() method stops recording audio. The release() method releases the MediaRecorder object.


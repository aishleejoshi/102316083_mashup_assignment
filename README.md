# Mashup Assignment

Name: Aishlee Joshi  
Roll Number: 102316083  

---

## 📊 Methodology

This project follows the below steps to generate the mashup:

### Step 1: User Input
The user provides the following inputs:

- Singer Name
- Number of videos (N)
- Duration of each audio clip (Y seconds)
- Output file name (for CLI)
- Email ID (for Web App)

These inputs are taken either through:
- Command Line Arguments (Program 1), or
- Web Form (Program 2).

---

### Step 2: Video Search and Download
The program uses the PyTube library to:

- Search YouTube videos related to the given singer name.
- Select the top N results.
- Download only the audio stream of each video.

This ensures faster download and reduced storage usage.

---

### Step 3: Audio Conversion
Each downloaded file is:

- Converted into audio format using PyDub.
- Processed using FFmpeg in the background.

This converts video files into usable audio clips.

---

### Step 4: Audio Trimming
Each audio file is trimmed to the first Y seconds.

This is done to:

- Maintain uniform duration.
- Reduce file size.
- Improve processing speed.

The trimmed clips are stored temporarily.

---

### Step 5: Audio Merging
All trimmed audio clips are merged sequentially into a single file.

- The AudioSegment class is used.
- All clips are appended in order.
- The final output is exported as an MP3 file.

---

### Step 6: Output Generation
The merged file is saved in MP3 format.

For CLI:
- Output file is saved in the local directory.

For Web App:
- A confirmation message is displayed (demo mode).

---

## 📋 Result Table

After execution, the program generates an output file.

Example Result Table (Command Line Execution):

| Parameter        | Value            |
|------------------|------------------|
| Singer Name      | Sharry Mann      |
| Videos Downloaded| 10               |
| Duration (sec)   | 20               |
| Output File      | output.mp3       |
| Status           | Success          |

This table represents the execution summary.

---

## 📈 Result Graph (Conceptual Representation)

The following graph represents the relationship between:

- X-axis: Number of Videos
- Y-axis: Processing Time (seconds)

Example Representation:


As the number of videos increases, processing time increases linearly.

This is due to increased download and conversion operations.

---

## 📊 Performance Analysis

| No. of Videos | Duration (sec) | Time Taken (Approx) |
|---------------|---------------|---------------------|
| 2             | 5             | 1 minute            |
| 5             | 10            | 3 minutes           |
| 10            | 20            | 7 minutes           |

Note: Performance may vary depending on internet speed and system resources.

---

## 🧪 Testing Methodology

The project was tested using:

- Small input values for initial testing.
- Medium input values for performance testing.
- Different singer names.
- Various duration values.

Edge cases tested:

- Invalid number of parameters.
- Non-numeric values.
- Incorrect file names.
- Internet connection failure.

---

## ⚠️ Limitations

- Processing speed depends on network bandwidth.
- Colab free version has limited resources.
- Large values of N may increase execution time.
- YouTube content availability may vary.

---

## ✅ Conclusion

The mashup system successfully:

- Automates video downloading.
- Converts videos to audio.
- Trims and merges audio files.
- Provides both CLI and Web interface.






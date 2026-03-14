# Video Summarizer

This is a Flask app that detects humans in uploaded videos and creates a summary video composed of detected frames.

Quick start (Windows):

1. Create and activate virtualenv
   - `python -m venv venv`
   - `.\
ev\Scripts\Activate` (PowerShell: `.
venv\Scripts\Activate`)
2. Install dependencies
   - `pip install -r requirements.txt`
3. Ensure `ffmpeg` is installed and on PATH (`ffmpeg -version`)
4. Run the app
   - `python app.py` or double-click `run.bat`
5. Open http://127.0.0.1:5000/ and upload a video

Notes and troubleshooting:
- If the app can't load YOLO models, a startup check runs automatically and will attempt a safe cfg cleanup. If it fails, check `~/.cvlib/object_detection/yolo/yolov3/` for `yolov4-tiny.cfg` and `yolov4-tiny.weights`.
- If files are missing you can enable automatic download by setting the environment variable `AUTO_DOWNLOAD_YOLO=1` before running the app; the app will attempt to download the official `yolov4-tiny.cfg` and `yolov4-tiny.weights` to `~/.cvlib/object_detection/yolo/yolov3/`.


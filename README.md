# MediaPipe Pose and Curl Counter

A local webcam experiment with MediaPipe and OpenCV. The notebook explores pose and hand landmarks before using shoulder, elbow, and wrist positions to estimate elbow angle and count curl repetitions.

[Open the notebook](mediapipe-curl-counter.ipynb)

## Run locally

From the repository root, use a fresh Python 3.11 environment.

```bash
python -m pip install -r requirements.txt
python -m jupyterlab
```

Run Jupyter on a desktop with a webcam and access to OpenCV preview windows. Run camera cells individually, keep the relevant arm in frame, and press `q` in the preview window to end a demo before starting the next one.

## What to inspect

| Demo | Output |
| --- | --- |
| Pose landmarks | Detected body landmarks drawn over the webcam feed. |
| Hand landmarks | Landmark overlays for visible hands. |
| Curl counter | Joint angle, movement stage, and repetition count drawn on the frame. |

The counter uses angle thresholds and a stage transition. Camera placement, occlusion, and unstable landmarks can change the count. Use the overlay to see how those conditions affect the result.

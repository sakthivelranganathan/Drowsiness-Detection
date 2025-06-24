Driver Drowsiness Detection and Emergency Alert System (Python + OpenCV)

This project implements a real-time driver drowsiness detection system using computer vision (OpenCV) and automatically triggers an emergency alert if the driver remains unresponsive for a certain period. 
The system also retrieves approximate location data using IP-based geolocation.

 Features

- Real-time driver face and eye detection using OpenCV Haar cascades
- Continuous monitoring of eye closure to detect drowsiness
- Configurable sleep threshold and emergency response time
- Beeping alarm when drowsiness is detected
- Simulated emergency contact alert after prolonged unresponsiveness
- Location tracking via IP geolocation (approximate)

Files

- `driver_drowsiness_emergency.py` → Main Python script
- `README.md` → This documentation

 Requirements

- Python 3.x
- OpenCV (`opencv-python`)
- `requests` package for geolocation API

 Install dependencies:

```bash
pip install opencv-python requests




How it works

1. The system captures live video using the webcam.
2. Face and eyes are detected in each frame using Haar cascade classifiers.
3. If eyes remain closed for a continuous threshold of frames, a beeping sound is triggered.
4. If the driver remains asleep for a longer configured time (30 seconds), an emergency alert is simulated:

   * Displays emergency message in the console.
   * Retrieves approximate location using `ipapi.co` IP geolocation service.
   * Prints emergency contact information.


Configuration

* `SLEEP_THRESHOLD`: Number of frames before the first beeping alert.
* `EMERGENCY_THRESHOLD_SEC`: Number of seconds of continuous sleep before triggering emergency.
* `EMERGENCY_CONTACT`: Replace with actual emergency mobile number.



Limitations

* Location accuracy depends on IP geolocation and may not be suitable for real-world deployment.
* No real SMS or phone call functionality included in this version.
* Requires active internet connection for geolocation API.



Future Improvements

* Integrate mobile GPS location for exact position (instead of IP-based).
* Integrate Twilio API for real phone calls and SMS alerts.
* Add deep learning-based drowsiness detection (CNN or YOLO for higher accuracy).
* Full vehicle integration with seat belt and engine status sensors.





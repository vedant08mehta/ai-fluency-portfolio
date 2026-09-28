2. Moodify — Emotion-Based Music Recommendation
The Problem

I wanted to experiment with making music recommendations based on a person's current emotional state, rather than requiring them to manually search for something that matches their mood.

The Approach

I built Moodify, a Streamlit web application that uses a webcam image to detect facial emotion and then recommends music based on the detected emotion.

For emotion detection, I integrated DeepFace's pretrained emotion-recognition model. I then connected the detected emotion to a rule-based playlist recommendation system.

How It Works

Webcam image → Emotion detection → Detected mood → Playlist recommendation

The application provides a simple interface where the user can interact with the system and receive a recommendation based on the detected emotion.

What I Built

The main work was integrating the pretrained computer-vision model into a working application and connecting its output to the recommendation logic.

I did not train a separate emotion-recognition model or conduct a formal user study, so I don't claim measured recommendation accuracy or real-world impact.

What I Learned

Moodify helped me understand how pretrained AI models can be integrated into an end-to-end application. It also showed me the difference between getting an ML model to produce a prediction and building an actual user-facing experience around that prediction.

# PoseAI

PoseAI is an iOS concept app for bodybuilding pose coaching. It uses on-device body landmark detection to help athletes practice mandatory poses, understand their weak points, and track progress over time.

This repository is a public product showcase. The production source code is private while the project is under active development.

## Product Overview

Bodybuilding posing is highly technical, but feedback is often limited to coaches, mirrors, or reviewing videos after the fact. PoseAI explores a more immediate workflow: point the phone at the athlete, choose a pose, hold the position, and receive focused feedback on the most important correction.

The app is designed around:

- Live pose coaching using the iPhone camera.
- Photo-based pose analysis for saved images.
- Pose-specific scoring for bodybuilding fundamentals.
- Progress tracking across practice sessions.
- Privacy-friendly, on-device analysis.

## Key Features

- **Live Coach:** Real-time pose tracking with front and rear camera support.
- **Pose Scoring:** Weighted scoring for execution, symmetry, stability, and detection confidence.
- **Coaching Cues:** The app identifies the weakest metric and turns it into a clear correction.
- **Photo Analysis:** Athletes can import a still image and receive the same scoring breakdown.
- **Progress Dashboard:** Saved sessions show score trends, recent analyses, and visual snapshots.
- **Hands-Free Flow:** Live practice is designed around stable holds rather than tapping buttons mid-pose.

## How The Scoring Works

PoseAI detects body landmarks such as shoulders, elbows, wrists, hips, knees, ankles, neck, and torso root. Those points are converted into normalized measurements so the app can compare poses across different body sizes, camera distances, and screen resolutions.

Examples of derived measurements include:

- Elbow flare compared to shoulder width.
- Wrist height compared to the waist line.
- Shoulder level relative to torso height.
- Stance width compared to shoulder width.
- Lat-to-waist ratio for front lat spread.
- Stability across recent frames.

Each bodybuilding pose has its own target ranges and weights. For example, a front lat spread prioritizes elbow flare and lat-to-waist ratio, while a side chest prioritizes torso rotation, chest height, arm setup, and stability.

## Tech Stack

- Swift
- SwiftUI
- Apple Vision
- AVFoundation
- Xcode

## Screenshots

| Live Coach | Pose Analysis | Progress |
| --- | --- | --- |

## Product Status

PoseAI is currently in prototype development. The current focus is improving pose-tracking stability, tightening scoring quality, refining camera orientation behavior, and making live coaching feel calmer and more useful during practice.

## Repository Note

This public repository intentionally excludes source code, proprietary scoring details, training data, product roadmap specifics, and private implementation files.

The source code for this project is kept private because the app is being developed as a potential product. Code samples or a walkthrough can be provided upon request.

For collaboration or investment conversations, please contact the project owner directly.

Contact: juanpablovillalba02@gmail.com 
linkedin: https://www.linkedin.com/in/juanpablovillalbaa/


# Technical Overview

This document describes the architecture at a high level without exposing private source code.

## Pose Detection

PoseAI uses Apple's on-device Vision framework to detect human body landmarks from camera frames or still images. The app reads normalized 2D joint coordinates for major body points such as shoulders, elbows, wrists, hips, knees, ankles, neck, and torso root.

## Normalization

Raw screen pixels are not used directly for scoring. The app converts body positions into normalized ratios, such as elbow width divided by shoulder width or shoulder height difference divided by torso height. This makes scoring more consistent across phone models, image sizes, body sizes, and camera distances.

## Pose Metrics

The app turns detected joints into bodybuilding-specific metrics, including:

- Elbow flare.
- Arm symmetry.
- Shoulder level.
- Wrist-to-waist alignment.
- Stance width.
- Torso rotation.
- Lat-to-waist ratio.
- Stability over recent frames.

## Scoring

Each pose defines target ranges for the metrics that matter most. A component score is calculated for each metric based on how close the athlete is to the target interval. The final score combines execution, symmetry, stability, and detection confidence.

## Coaching Cues

The app ranks failed checks by severity and selects the highest-priority issue as the live cue. This keeps feedback focused instead of overwhelming the athlete with too many corrections at once.

## Live Coaching

The live camera flow includes smoothing, movement gating, hold detection, cue throttling, and short-term joint memory. This helps reduce jitter, avoids constant cue spam, and makes side poses more stable when some body parts are temporarily occluded.

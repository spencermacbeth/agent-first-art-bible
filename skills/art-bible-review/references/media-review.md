# Review conditions by medium

Use the rows relevant to the task. These are decision criteria, not a required technology stack.

| Medium | Candidate inspection | Integration inspection |
| --- | --- | --- |
| Images | Full-resolution view, crop/zoom, intended dimensions and clear reference pairing | Final display size, UI overlays, contrast and composition in the actual screen |
| 3D | Orbit controls, declared units/scale, material and lighting checks, all relevant sides | Production camera, environment lighting, footprint, occlusion, animation and target performance |
| Video | Scrubbing, sound controls, captions where relevant, repeatable ranges around cuts | Actual crop, frame rate, transitions, surrounding audio and delivery playback |
| Sound | Explicit gain, repeatable A/B playback, original and any normalized derivative, loop and tail checks | Trigger timing, overlaps, mix, device speakers/headphones and intended emotional function |
| Writing | Voice, vocabulary, intended meaning, alternatives beside the relevant setting and rules | Actual text length, surrounding copy and UI; a line should preserve the rule or story distinction it conveys |
| Interface | Hierarchy, typography, color roles and states using representative content | Real display size, interaction, focus and motion; check whether the player can understand and act on the information |

An isolated model viewer is useful for geometry but can hide problems with the scene camera or lighting. Make a representative scene containing the relevant gameplay geometry and UI early enough to affect selection.

Record the conditions that affect the comparison. For a model this might include camera pose, renderer version, exposure, light setup, scale and animation state. For sound it may include gain, normalization, event context and output device. Hold camera and gain fixed when comparing candidates; vary them deliberately when robustness to those conditions is itself the question.

Examples of stack choices:

- A static HTML gallery can handle images and playable video/audio with exported feedback.
- A web GLB viewer can serve isolated 3D inspection when the runtime also supports those assets.
- An engine-native scene is preferable when a web preview cannot reproduce the game's shaders, lighting or camera behavior.
- Local filesystem writes through a small server can support persistent reviews, but keep it bound to the intended interface and limit what it can read or write. Provider credentials stay outside the browser.

Optimization is part of the reviewed pipeline. Compare a compressed or simplified derivative with its source at the size and angles that matter. Record the transform instead of treating the smaller file as an equivalent master.

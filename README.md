# Projector Correction Project
#### Kincannon Wilson, James Wedum, Nithin Weerasinghe

### Presentation Slides

### Intro
  The project aims to develop and evaluate methodologies for improving the quality of projected images by adapting to environmental factors such as lighting conditions, surface color, and texture. The goal is to create an application capable of intelligently enhancing projected image quality.

Current projectors utilize basic color correction algorithms and smooth screens to enhance image quality, but they don't effectively address changing environmental conditions like surface texture or dynamic factors such as moving screens or shifting lighting. Past research often relies on specialized hardware or algorithms, limiting accessibility. Our project proposes a dynamic correction system that adapts to environmental changes using only a camera, projector, and computer connected via HDMI, eliminating the need for specialized hardware like GPUs or constant user input.

### Methodology (method, data, evaluation metrics). If applicable, highlight how it differs from prior work (new experiments, new methods, etc)
#### Method
- Reactive-Adaptive Control System
  - Feed-forward controller for image shape
  - Feed-back controller for color correction
- Low-pass filter
  - Attenuate high-frequency information (such as motion)
  - Focus on low-frequency delta (background/environment color)
- PD controller for motor with rotary encoder for real-time focus adjustment
  - Potential correction for rapid perturbations, such as the projector being struck
- Single-sensor, low-cost option
  - Dual-sensor with rotary encoder
#### Data

For testing purposes, we primarily used a scene from *The Wolf of Wall Street (2013)*.

#### Evaluation Metrics
The team has created one metric for evaluating the effectiveness of various experiments. This metric measures the distance between a recorded image and the actual image. It is calculated by taking the absolute difference between the two images’ intensities and dividing by the maximum possible difference between two images of that size to obtain a result in the range of 0 to 1, inclusive. 

After working on the project, we realized that this may not be the best approach as it does not adaquately take into account image artifacts which is very noticeable for the average viewer. Other prior works have utilized user studies to corroborate their results by having users compare the resulting projection against a control or other techniques. Given the time and resource constraints, we were not able to conduct such trials.


### Discussion of quantitative results
### Demos

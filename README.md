# Efficient Trajectory Optimization for Autonomous Racing via Formula-1 Data-Driven Initialization

This repository contains the official implementation for the paper:

**Efficient Trajectory Optimization for Autonomous Racing via Formula-1 Data-Driven Initialization**  
Samir Shehadeh, Lukas Kutsch, Nils Dengler, Sicong Pan, Maren Bennewitz

## Overview

Trajectory optimization is a key component of autonomous racing, but practical minimum-time optimization pipelines can be highly sensitive to the initial trajectory. Poor initialization, such as using the track centerline or purely geometric baselines, may lead to slow convergence or suboptimal local solutions.

This work proposes a learning-informed initialization strategy that uses expert Formula 1 telemetry as a prior for autonomous racing trajectory optimization. The method reconstructs and aligns real-world Formula 1 racelines across multiple tracks, trains a neural network to predict expert-like raceline offsets from local track geometry, and uses the predicted raceline as an initialization seed for a minimum-time optimal control solver.

## Key Ideas

- Reconstruction of expert Formula 1 racelines from telemetry data.
- Standardized track-centered representation using centerline arc length, curvature, track boundaries, and lateral raceline offsets.
- Neural raceline prediction from local track geometry.
- Learned initialization for minimum-time trajectory optimization.
- Evaluation across 17 Formula 1 tracks.
- Hardware validation on a 1:10 RoboRacer platform.

## Repository Status

🚧 **Code coming soon.**

This repository is currently a placeholder. The cleaned and documented code will be released here soon.

Planned contents include:

- Dataset processing and raceline reconstruction tools
- Track representation utilities
- Neural raceline prediction model
- Training and evaluation scripts
- Minimum-time optimization initialization interface
- RoboRacer-related validation utilities
- Example configurations and usage instructions

## Method Summary

The full pipeline consists of three main stages:

1. **Formula 1 telemetry processing**  
   Real-world Formula 1 telemetry is reconstructed, aligned to track geometry, and converted into a Frenet-frame representation.

2. **Learning-based raceline prediction**  
   A neural network predicts expert-like raceline offsets from local track features such as curvature and track boundary offsets.

3. **Minimum-time trajectory optimization**  
   The predicted raceline is used as an informed initialization for a physics-based minimum-time optimal control solver.

## Citation

If you use this work, please cite the paper:

```bibtex
@inproceedings{shehadeh2026efficient,
  title     = {Efficient Trajectory Optimization for Autonomous Racing via Formula-1 Data-Driven Initialization},
  author    = {Shehadeh, Samir and Kutsch, Lukas and Dengler, Nils and Pan, Sicong and Bennewitz, Maren},
  booktitle = {IEEE International Conference on Intelligent Transportation Systems (ITSC)},
  year      = {2026}
}
```

## License

The license will be added with the code release.

## Contact

For questions, please open an issue once the repository is public or contact the authors directly.

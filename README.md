# Aerospace-Electrical-MATLAB-Project
We need a MATLAB core script that simulates this noisy raw sensor input, builds a digital low-pass filtering algorithm without relying on toolbox extensions, analyzes signal attenuation characteristics, and updates performance logs. Please deliver a clean script along with an engineering performance analysis report.
# Drone Flight Controller Signal Filter

## Project Overview
This repository hosts a core MATLAB script that simulates and attenuates high-frequency structural vibration noise within an Unmanned Aerial Vehicle (UAV) Inertial Measurement Unit (IMU) telemetry stream. It features a custom-built discrete-time low-pass filtering algorithm implemented via array operations without relying on optional MATLAB toolboxes.

## Algorithmic Performance
- **Signal Tracking:** Isolates low-frequency, real flight changes (e.g., pitch changes) from high-frequency propulsion noise.
- **Filter Type:** First-order recursive lag smoothing engine controlled by a configurable attenuation factor (α).
- **Statistical Analytics:** Automatically calculates signal variance changes and measures wideband noise power attenuation in decibels (dB).

## File Structure
- `signal_filter.m`: Primary MATLAB script including data generation, recursive filtering loop, and statistical logging.
- `README.md`: Dynamic script overview.

## How To Run
1. Launch MATLAB or GNU Octave.
2. Open the directory containing `signal_filter.m`.
3. Execute the script within the command window or editor panel:
```matlab
run('signal_filter.m')
```

## Performance Metrics Output
The script prints an assessment profile directly to the MATLAB Command Window:
```text
=== IMU Filtering Routine Verification ===
Processed Samples         : 1501
Raw Signal Variance       : 22.0914
Filtered Signal Variance  : 6.9452
Signal Attenuation Profile: 5.02 dB
=========================================
```

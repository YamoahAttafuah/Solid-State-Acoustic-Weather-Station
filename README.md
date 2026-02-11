# Solid-State Weather Station: Measuring Wind with Sound

**Author:** Yamoah Frimpong Attafuah  
**Project:** Capstone Engineering Research  

---

## Video Demo
https://github.com/user-attachments/assets/21c24ba8-04c9-482c-a180-2cb9e2079cd8

---

## Device Gallery
![Mounted Weather Station POV 1](https://github.com/user-attachments/assets/8d539d3b-d519-42f7-8126-9c2f4cc28eea)
*Figure 1: The mounted weather station performing wind measurements.*

![Mounted Weather Station POV 2](https://github.com/user-attachments/assets/d8af3a0a-aa8a-456a-b571-55d701b52fc7)
*Figure 2: A slightly different POV of the mounted weather station performing wind measurements.*

---

## Project Overview
Traditional weather stations rely on mechanical anemometers (cups and vanes) to measure wind speed and direction. These moving parts are susceptible to mechanical wear, friction, and degradation in harsh weather conditions.

This project presents a novel Solid-State Weather Station that eliminates moving parts by using sound to measure wind properties. By analyzing the wind noise captured by an array of microphones, Machine Learning (ML) models are employed to accurately estimate Wind Speed and classify Wind Direction, offering a durable, low-maintenance alternative for weather monitoring.at Ashesi University.

---

## Proprietary Notice
This repository serves as a portfolio showcase of the hardware design and research outcomes. The source code, datasets, and specific model architectures are currently proprietary and are being utilized for further research and development 

---

## Hardware Architecture
The system is built around a microcontroller and a 4-microphone array arranged in a specific geometry (North, South, East, West) to capture directional wind noise.

* **Microcontroller**: Nano RP2040.

* **Sensors**: 4x MAX4466 Electret Microphone Amplifiers.

* **Power**: Solar panel and battery management system for autonomous operation.

* **Connectivity**: WiFi/MQTT for data transmission.

---

## Software & Firmware
* **Embedded**: C++ for data acquisition and transmission.

* **Machine Learning & Edge AI**: Python, TensorFlow (ANN, CNN), Scikit-Learn (Random Forest, Gradient Boosting, LightGBM), LiteRT (Model Compression).

* **Signal Processing**: Librosa (Audio feature preprocessing and extraction: MFCCs, Spectral Centroid, ZCR).

* **Data Analysis**: Pandas, NumPy, Jupyter Notebooks.

* **Communication**: MQTT (Message Queuing Telemetry Transport) & Wi-Fi for data logging.

---

### Key Features
- **No Moving Parts:** Significantly increases durability in harsh environments.  
- **Audio-Based Sensing:** Uses commercial off-the-shelf (COTS) electret microphones.  
- **Edge/Cloud AI:** Utilizes ML models to interpret complex aeroacoustic signatures.
- **High Accuracy:** Achieved wind speed estimation comparable to commercial mechanical anemometers.

---

## Performance Results
The system was validated against a reference commercial weather station. The machine learning models achieved the following performance metrics:

### Wind Speed Estimation
- **Models:** ANN & Random Forest Regressor
- **Root Mean Square Error (RMSE):** 0.58 m/s
- **Mean Absolute Error (MAE):** 0.36 m/s

### Wind Direction
- **Models:** CNN, Gradient Boosting & LightGBM
- **Classification Accuracy:** ~81% (Across 8 cardinal directions: N, NE, E, SE, S, SW, W, NW)  

---

## Acknowledgements
Supervised by Dr. Nathan Amanquah.

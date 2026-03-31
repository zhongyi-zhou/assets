# TFLite Models Repository

This repository hosts TFLite models used in the `xrblocks` project. Please see the following instructions on how to contribute your model.

---

## 📖 Instructions for Adding a New Model

To add a new TFLite model to this repository, follow these steps:

1. **Upload the TFLite File**: Put the `.tflite` file under the appropriate category folder (e.g., `gestures/`). If you want to propose a new folder, please justify the name of the folder and explain how it may also fit for future models.
2. **Update this README.md**: Add a new section for the model with a clear "Model Card" containing the following info:
   - **Model Name**: Filename of the `.tflite` model.
   - **Description**: What does this model do?
   - **Input/Output**: Data Type and Shape.
   - **Labels / Classes**: What are the outputs if it's a classification model?

---

## ✋ Gestures Models

### `xr_emoji.tflite`
Custom hand gesture classification model using relative bone angles. Detects 7 gesture classes.

- **Description**: Classify hand gestures based on relative bone angles.
- **Input/Output**:
  - **Input**: Type `float32`, Shape `[1, 19, 1]` (where 19 is the number of relative bone angles).
  - **Output**: Type `float32`, Shape `[1, 7]` (probabilities for 7 gesture classes).
- **Gesture List**:

| Index | Label / Gesture | Description / Context |
| :--- | :--- | :--- |
| **0** | `OTHER` | Unrecognized or default pose |
| **1** | `FIST` | A closed fist (used as "Rock" in Rock-Paper-Scissors) |
| **2** | `THUMB UP` | Thumbs Up (or Down depending on angle / axis) |
| **3** | `POINT` | Pointing index finger |
| **4** | `VICTORY` | Peace sign (used as "Scissors" in Rock-Paper-Scissors) |
| **5** | `ROCK` | The "Horns" or Rock sign (separate from the closed Fist) |
| **6** | `SHAKA` | "Hang Loose" gesture |


# Doordarshi 👁️✨ - AI Vision for the Visually Impaired

**An offline, Edge-AI wearable to help the blind perceive surroundings and read printed text without relying on the internet.**

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

<br>

> Doordarshi (दूरदर्शी) means "visionary" or "one who can see far". This project empowers the visually impaired with an artificial eye and a voice that describes the world, all in a compact, offline device.

<br>

<p align="center">
  <img src="YOUR_PROJECT_IMAGE_OR_GIF_URL_HERE" alt="Project Demo" width="600"/>
</p>

---

## 🚀 Core Features

* **🤖 On-Device Scene Description:** Understand your surroundings in real-time. With the push of a button, get a rich, audible description of what's in front of you. Powered by the lightweight yet powerful **MoonDream** model.

* **📄 Instant Text Reading (OCR):** Read menus, documents, or signs effortlessly. The device uses **Tesseract OCR** to accurately extract and read printed text aloud.

* **🌐 100% Offline Functionality:** No internet? No problem. All processing happens directly on the device, ensuring privacy, speed, and reliability anywhere, anytime.

* **💡 Robust Vision with OpenCV:** Achieves reliable scene perception and **80-90% OCR accuracy** across diverse and challenging lighting conditions, thanks to advanced image processing with OpenCV.

* **🔊 Real-time Audio Feedback:** All descriptions and text are converted to speech, providing an intuitive and seamless user experience.

---

## 🛠️ Tech Stack & Architecture

The entire system runs on a low-power, portable setup, making it a true edge-computing solution.

| Component | Technology | Role |
|---|---|---|
| **Compute** | ![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22846?style=for-the-badge&logo=raspberry-pi&logoColor=white) | The brain of the operation; handles all processing. |
| **Vision** | ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white) | Image capture, pre-processing, and optimization. |
| **Perception** | ![Ollama](https://img.shields.io/badge/MoonDream_(Ollama)-000000?style=for-the-badge&logo=ollama&logoColor=white) | On-device multimodal model for scene descriptions. |
| **Text Reading**| ![Tesseract](https://img.shields.io/badge/Tesseract_OCR-1FB2A7?style=for-the-badge) | High-accuracy Optical Character Recognition engine. |

---

## ⚙️ How It Works

The workflow is simple and efficient:

1.  **Trigger**: The user presses a button on the wearable.
2.  **Capture**: The Raspberry Pi camera captures a high-resolution image of the user's view.
3.  **Process**: OpenCV pre-processes the image (e.g., noise reduction, contrast adjustment) to enhance clarity.
4.  **Infer**:
    * For **Scene Description**, the image is passed to the **MoonDream** model running via Ollama.
    * For **Text Reading**, the image is passed to the **Tesseract OCR** engine.
5.  **Respond**: The generated text is converted into speech and played back to the user through headphones.

---

## 🚀 Getting Started

### Prerequisites

* Raspberry Pi (Model 4 or newer recommended)
* Raspberry Pi Camera Module
* Power Bank
* Headphones/Speaker
* Required dependencies (Python, OpenCV, etc.)

### Installation

1.  Clone the repository:
    ```bash
    git clone [https://github.com/Chetan00000/doordarshi.git](https://github.com/Chetan00000/doordarshi.git)
    cd doordarshi
    ```

2.  Install required Python packages:
    ```bash
    pip install -r requirements.txt
    ```

3.  Setup Ollama and pull the MoonDream model:
    ```bash
    # Follow instructions on the Ollama website to install
    ollama pull moondream
    ```

### Usage

Run the main script from your terminal:
```bash
python main.py

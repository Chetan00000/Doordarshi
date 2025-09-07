Doordarshi 👁️✨ - AI Vision for the Visually Impaired
An offline, Edge-AI wearable to help the blind perceive surroundings and read printed text without relying on the internet.

<br>

Doordarshi (दूरदर्शी) means "visionary" or "one who can see far". This project empowers the visually impaired with an artificial eye and a voice that describes the world, all in a compact, offline device.

<br>




🚀 Core Features
🤖 On-Device Scene Description: Understand your surroundings in real-time. With the push of a button, get a rich, audible description of what's in front of you. Powered by the lightweight yet powerful MoonDream model.

📄 Instant Text Reading (OCR): Read menus, documents, or signs effortlessly. The device uses Tesseract OCR to accurately extract and read printed text aloud.

🌐 100% Offline Functionality: No internet? No problem. All processing happens directly on the device, ensuring privacy, speed, and reliability anywhere, anytime.

💡 Robust Vision with OpenCV: Achieves reliable scene perception and 80-90% OCR accuracy across diverse and challenging lighting conditions, thanks to advanced image processing with OpenCV.

🔊 Real-time Audio Feedback: All descriptions and text are converted to speech, providing an intuitive and seamless user experience.

🛠️ Tech Stack & Architecture
The entire system runs on a low-power, portable setup, making it a true edge-computing solution.

Component	Technology	Role
Compute		The brain of the operation; handles all processing.
Vision		Image capture, pre-processing, and optimization for accuracy.
Perception		On-device multimodal model for generating scene descriptions.
Text Reading		High-accuracy Optical Character Recognition for reading printed text.

Export to Sheets
⚙️ How It Works
The workflow is simple and efficient:

Trigger: The user presses a button on the wearable.

Capture: The Raspberry Pi camera captures a high-resolution image of the user's view.

Process: OpenCV pre-processes the image (e.g., noise reduction, contrast adjustment) to enhance clarity.

Infer:

For Scene Description, the image is passed to the MoonDream model running via Ollama.

For Text Reading, the image is passed to the Tesseract OCR engine.

Respond: The generated text description or the extracted text is converted into speech and played back to the user through headphones or a speaker.

Getting Started
Prerequisites
Raspberry Pi (Model 4 or newer recommended)

Raspberry Pi Camera Module

Power Bank

Headphones/Speaker

Required dependencies (Python, OpenCV, etc.)

Installation
Bash

# 1. Clone the repository
git clone https://github.com/your-username/doordarshi.git
cd doordarshi

# 2. Install required Python packages
pip install -r requirements.txt

# 3. Setup Ollama and pull the MoonDream model
# Follow instructions on the Ollama website to install
ollama pull moondream
Usage
Bash

# Run the main script
python main.py
Press the designated hardware button to trigger scene description or text reading.

🎯 Future Roadmap
[ ] Improve form factor for better ergonomics.

[ ] Add support for more languages.

[ ] Implement specific object detection (e.g., "find my keys").

[ ] Enhance battery optimization.

🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

📜 License
This project is licensed under the MIT License. See the LICENSE file for details.

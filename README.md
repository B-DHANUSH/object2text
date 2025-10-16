# Image Description Generator

A Python project that generates detailed descriptions for images by combining **object detection**, **image captioning**, and **text summarization**. The pipeline detects objects in an image, generates a caption, and produces a concise description saved to a text file.

---

## Features

- **Object Detection:** Uses YOLOv8 to detect objects in images.
- **Image Captioning:** Generates captions using Salesforce BLIP model.
- **Description Generation:** Summarizes captions into short 2–3 line descriptions using `T5-small`.
- **Output:** Saves detected objects, captions, and descriptions as text files.
- **Fully Automated Pipeline:** Process multiple images in a folder and generate results automatically.

---

## Architecture

![Architecture Diagram](assets/architecture.png)

**Flow Description:**

1. **Input Image:** User provides an image in the `input/` folder.
2. **Object Detector:** Detects objects using YOLOv8.
3. **Image Captioner:** Generates a descriptive caption for the image using BLIP.
4. **Description Generator:** Summarizes the caption into a short, detailed description using T5-small.
5. **File Manager:** Saves the detected objects, caption, and description as a text file in `output/`.

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/B-DHANUSH/image-description-generator.git
cd image-description-generator

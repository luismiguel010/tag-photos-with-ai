# Tag Photos with AI

Image captioning application using the BLIP model (Bootstrapping Language-Image Pre-training) from Hugging Face with a Gradio web interface. Based on the Coursera IBM guided project "Give Meaningful Names to Your Photos with AI".

## What's included

| Script | Description |
|---|---|
| `hello.py` | Gradio hello world demo |
| `image_cap.py` | Basic script — generates a caption for a local image |
| `image_captioning_app.py` | Web app — upload an image and get a caption via Gradio |
| `automate_url_captioner.py` | Scrapes images from a URL and generates captions for each one |

## Setup

```bash
# Create and activate virtual environment
python3 -m venv my_env
source my_env/bin/activate

# Install dependencies
pip install -r requirements.txt
```

## Usage

### Gradio web app (main)

```bash
python image_captioning_app.py
```

Open http://localhost:7860, upload any image, and get a caption.

### Basic captioning script

```bash
# Place an image named sample.jpg in the project directory, then:
python image_cap.py
```

### Automated URL captioner

```bash
python automate_url_captioner.py
```

Scrapes images from a webpage (default: Wikipedia/IBM) and saves captions to `captions.txt`.

## Tech stack

- **BLIP** — `Salesforce/blip-image-captioning-base` from Hugging Face
- **Gradio** — web interface
- **PyTorch** — deep learning backend
- **BeautifulSoup** — HTML parsing for URL captioner

# AI Character Design and Diagram Experiments

A Google Colab notebook exploring Python-based diagram generation and AI-assisted character design. The notebook includes graph and entity-relationship diagram examples, language-model-based character analysis and prompt generation, and text-to-image generation experiments.

## What the notebook contains

### 1. Diagram and graph examples
- Builds an entity-relationship diagram for students, courses, and enrollments with Graphviz.
- Creates a simple network topology using NetworkX and Matplotlib.
- Calculates graph statistics and a shortest path between network nodes.
- Includes small Turtle and Matplotlib drawing experiments.

### 2. Character analysis and prompt generation
- Loads the `Qwen/Qwen2.5-3B-Instruct` language model with Hugging Face Transformers.
- Defines helper functions to ask the model questions, extract character attributes, and expand descriptions into image-generation prompts.
- Builds character specifications covering appearance, clothing, weapons, abilities, personality, and art style.

### 3. Text-to-image experiments
- Experiments with Hugging Face Diffusers pipelines, including FLUX.1-schnell, SDXL Turbo, and SD-Turbo.
- Creates prompts for character design sheets with front, side, and back views.
- Displays generated images in the notebook.

## Technologies

- Python
- Google Colab / Jupyter Notebook
- PyTorch
- Hugging Face Transformers
- Hugging Face Diffusers
- Accelerate
- SentencePiece
- Graphviz
- NetworkX
- Matplotlib
- Pillow / IPython display

## Setup

The notebook was originally written for Google Colab. For the AI model cells, use a GPU runtime with sufficient GPU memory.

1. Open `diagram.ipynb` in Google Colab.
2. Select **Runtime → Change runtime type** and choose a GPU runtime if available.
3. Run the notebook cells in a suitable order.
4. Install the Python packages required by the cells, for example:

   ```bash
   pip install transformers accelerate diffusers sentencepiece
   pip install torch torchvision
   pip install graphviz networkx matplotlib
   ```

   Graphviz may also require its system executable. In Google Colab, this can be installed with `apt-get` if needed.

## Important notes

- This repository is notebook-based; it does not currently include a standalone `app.py` application.
- The notebook contains several experiments and alternative model pipelines rather than one fully integrated workflow. Some cells redefine variables or delete models to free GPU memory, so execute cells carefully and in the intended order.
- Model downloads can be large and require an internet connection. Some Hugging Face models may have additional access or license requirements.
- GPU availability and memory limits may affect which image-generation models can run.
- The notebook's diagram examples are separate from the character-generation experiments.

## Project structure

```text
ai-character-design-project/
├── diagram.ipynb
├── README.md
└── requirements.txt
```

## Possible next steps

- Separate diagram demonstrations from the character-generation workflow.
- Combine character analysis, prompt generation, and image generation into a single, ordered pipeline.
- Add input validation and save generated images to an output directory.
- Create a simple Gradio interface once the notebook workflow is stable.

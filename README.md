# 🏛️ Enterprise AI Governance with IBM Granite

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/malinowski-marek/Governed-Granite-Summarizer/blob/main/Governed_Granite_Summarizer.ipynb)

Explore an enterprise AI governance use case with the open-source **IBM Granite 3.0 8B Instruct** model. This notebook loads the model in 4-bit precision and uses it to summarize a sample corporate data-protection policy and highlight potential compliance risks.

> **Quick start:** Open the notebook in Google Colab using the badge above. Select a GPU runtime (such as a T4), then run the cells in order.

## Repository contents

- **`Governed_Granite_Summarizer.ipynb`** — Interactive notebook for Google Colab or Jupyter.
- **`README.md`** — Project overview and usage instructions.

## What the notebook demonstrates

- Loading IBM Granite 3.0 8B Instruct with Hugging Face Transformers.
- Configuring 4-bit quantization with `bitsandbytes` to reduce memory use.
- Formatting a compliance-assistant prompt with Granite's tokenizer chat template.
- Generating a concise summary of a mock data-protection policy, including potential risks.

## Run in Google Colab

1. Open the notebook with the **Open in Colab** badge above.
2. In Colab, choose **Runtime → Change runtime type → T4 GPU** (or another available GPU).
3. Run the cells from top to bottom. The first cells install dependencies and download the model, which may take a few minutes.

The notebook installs `transformers`, `accelerate`, and `bitsandbytes`. A compatible GPU runtime is recommended for quantized model loading and inference. Availability of free GPU hardware depends on Google Colab.

## Run locally

Use a Python environment with a compatible CUDA GPU, then install the notebook dependencies:

```bash
pip install torch transformers accelerate bitsandbytes
```

Download or clone this repository, open `Governed_Granite_Summarizer.ipynb` in Jupyter, and execute the cells in order. Model download and GPU memory requirements apply locally as well.

## Governance context and limitations

The example illustrates how a language model can assist with policy summarization; it is **not** a production governance integration. The notebook does not connect to watsonx.governance, register an AI use case, or create an auditable factsheet. Those integrations require separate configuration and implementation.

Model output can be incomplete or incorrect. Treat summaries as decision-support only, verify them against the source policy, and do not use this sample to make compliance or employment decisions. Avoid sending real confidential or personal data to an unapproved environment.

## Model

The notebook uses [`ibm-granite/granite-3.0-8b-instruct`](https://huggingface.co/ibm-granite/granite-3.0-8b-instruct) from Hugging Face. Review the model card and applicable license and usage terms before use.

---

**Made for educational exploration of IBM Granite and AI governance.**

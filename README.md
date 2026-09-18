# Hello there! 👋

I’m **Carlos**, an **AI Architect** and **Recommendation Systems Lead** building end-to-end AI systems, from custom neural architectures to production recommendation platforms. What drives me is solving real problems through data-driven automation.

🔗 [Website](https://perez-malla.com) · [LinkedIn](https://www.linkedin.com/in/carlosuziel/) · [Google Scholar](https://scholar.google.com/citations?user=tEz_OeIAAAAJ)

🚀 **Currently (since September 2026):** leading recommendation systems as an AI Architect, making it easier to know which visas best fit each person that wants to enter Europe, with a heavy emphasis on knowledge graphs, LLMs and other modern AI methods.

## 🧬 Open Source

My projects are open source and free to use. The one I’m most involved with is [**pikaia**](https://github.com/danube-ai/pikaia), a freely accessible Python package for evolutionary algorithms, genetic programming and AI-driven optimization, open-sourced by [danube.ai](https://github.com/danube-ai) and available on [PyPI](https://pypi.org/project/pikaia/). As lead contributor I built the modular strategy system (12 gene strategies, 7 organism strategies), implemented the D-matrix accelerated iteration mode, and set up the CI/CD → PyPI release pipeline and the documentation site. I also researched genetic attention mechanisms for transformers there, with a white paper and an ablation study.

A few more, from research to playful AI:

| Project | What it is |
| --- | --- |
| [**goi-strat**](https://github.com/CarlosUziel/goi-strat) | Gene-of-interest-based sample stratification for evaluating functional differences, wiring Python together with R tools (DESeq2, limma, clusterProfiler) for differential expression, enrichment and PPI-network analysis, published in *BMC Bioinformatics* (2025). |
| [**pca_wgcna_ml**](https://github.com/CarlosUziel/pca_wgcna_ml) | Identifies TPX2-centered gene co-expression networks as drivers of aggressive prostate cancer, combining weighted gene co-expression network analysis (WGCNA) with machine learning over multi-omics data from TCGA and SU2C-PCF. |
| [**ischleseg**](https://github.com/CarlosUziel/ischleseg) | My MSc dissertation: segmenting ischemic stroke lesions in brain MRI with convolutional neural networks (DeepMedic) on the ISLES 2017 dataset, focused on the pre- and post-processing that moves the needle on accuracy. |
| [**doc-extractor**](https://github.com/CarlosUziel/doc-extractor) | Pulls structured data out of PDFs with multimodal LLMs (GPT-4o, Gemini), parsing documents into validated Pydantic schemas with optional bounding boxes to highlight where each value came from. |
| [**contexto-solver**](https://github.com/CarlosUziel/contexto-solver) | Solves the Contexto.me word game by navigating GloVe embeddings in a Qdrant vector database, using its Discovery API with positive and negative context pairs to close in on the secret word. |
| [**twenty-seven**](https://github.com/CarlosUziel/twenty-seven) | "The Council of the Twenty-Seven": a Next.js and FastAPI app that answers life questions through 27 philosophical lenses (inspired by Derek Sivers’ *How to Live*), using LLMs to synthesize the perspectives. |

## ⚡ How I Work

- **Systems-level thinking:** I enjoy architecting AI platforms end to end, from data ingestion and knowledge graphs through retrieval, ranking and serving, keeping the pieces coherent as they grow into many services.
- **Ship it, then sharpen it:** I get a simple version working first, then let profiling point me to the bottlenecks, which are often LLM calls I can replace with faster, more robust deterministic algorithms (usually embeddings instead of text generation).
- **Local-first, with CLIs worth using:** I like giving a system a beautiful [_Typer_](https://github.com/fastapi/typer) CLI/SDK that drives every service from the terminal, so I can build and test the whole stack locally before pointing the same client at the cloud.
- **Build things I can actually run:** I aim for reproducible infrastructure, observability and deployments meant for production, not just a demo.

## 🛠️ Tech Stack

I build on the **Python** ecosystem, end to end:

- **Backend & APIs:** I build async services with [_FastAPI_](https://github.com/fastapi/fastapi) and [_Pydantic_](https://github.com/pydantic/pydantic) for typed APIs, [_SQLModel_](https://github.com/fastapi/sqlmodel) and [_Alembic_](https://github.com/sqlalchemy/alembic) for the data layer and migrations, [_httpx_](https://github.com/encode/httpx) for service-to-service calls, and [_Typer_](https://github.com/fastapi/typer)/[_Rich_](https://github.com/Textualize/rich) for terminal-friendly CLIs.
- **LLMs & RAG:** I call providers directly to keep full control over prompts, context and retries, leaning on embeddings ([_Transformers_](https://github.com/huggingface/transformers), [_sentence-transformers_](https://github.com/UKPLab/sentence-transformers), [_fastembed_](https://github.com/qdrant/fastembed)) over generation where it’s enough and reaching for [_Haystack_](https://github.com/deepset-ai/haystack) or [_LangChain_](https://github.com/langchain-ai/langchain) only when they earn their place.
- **Inference:** A single config switch moves every LLM call between a hosted API (_Gemini_), a local [_llama.cpp_](https://github.com/ggml-org/llama.cpp) server and a self-hosted [_vLLM_](https://github.com/vllm-project/vllm) deployment, all behind one OpenAI-compatible interface.
- **Knowledge graphs & data:** [_Neo4j_](https://github.com/neo4j/neo4j) for knowledge graphs, [_Qdrant_](https://github.com/qdrant/qdrant) for vector search, [_PostgreSQL_](https://github.com/postgres/postgres) as the system of record, and [_MinIO_](https://github.com/minio/minio) for S3-compatible object storage.
- **ML & optimization:** [_PyTorch_](https://github.com/pytorch/pytorch) for custom models and research, [_scikit-learn_](https://github.com/scikit-learn/scikit-learn) and [_pandas_](https://github.com/pandas-dev/pandas) for classic ML and data wrangling, and [_pikaia_](https://github.com/danube-ai/pikaia) when evolutionary optimization beats gradient descent.
- **MLOps & observability:** [_MLflow_](https://github.com/mlflow/mlflow) as my registry and store for models, prompts and evaluation artifacts, with [_Prometheus_](https://github.com/prometheus/prometheus) for metrics and [_Loguru_](https://github.com/Delgan/loguru) for readable logging.
- **Ship & operate:** I containerize services with [_Docker_](https://github.com/moby/moby) and run them on [_Kubernetes_](https://github.com/kubernetes/kubernetes), describing the whole stack as code with [_Pulumi_](https://github.com/pulumi/pulumi) (in Python) on Hetzner Cloud.
- **Tooling & quality:** [_uv_](https://github.com/astral-sh/uv) for dependency management plus [_ruff_](https://github.com/astral-sh/ruff) and [_pyright_](https://github.com/microsoft/pyright) for linting and type-checking, all enforced through [_pre-commit_](https://github.com/pre-commit/pre-commit) and re-run in CI/CD with the full [_pytest_](https://github.com/pytest-dev/pytest) suite.

## 🎓 Education

I studied across three countries, and each degree wrapped up with a hands-on thesis:

- **PhD in Medical Informatics, Biostatistics and Complex Systems** (Distinction), Medical University of Vienna, with a doctoral thesis on prostate cancer research using machine learning.
- **MSc in Artificial Intelligence** (Distinction), University of Edinburgh, with a master’s thesis on ischemic stroke lesion segmentation using CNNs.
- **Double BSc in Computer Science and Business Management** (Extraordinary Award), Universidad de Las Palmas de Gran Canaria, with a bachelor’s thesis on facial emotion recognition with CNNs for neuromarketing.

## 📬 Get in Touch

Feel free to explore my repos, visit [perez-malla.com](https://perez-malla.com) or say hello on [LinkedIn](https://www.linkedin.com/in/carlosuziel/), and you can find my published research on [Google Scholar](https://scholar.google.com/citations?user=tEz_OeIAAAAJ).

👇 P.S. yes, that’s **UZIEL** spelled out across the contribution graph below.

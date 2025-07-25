# Useful Python Libraries (For Systems, ML/DL, and Utility Work)

##  System & Utility Libraries

| Library | Description | When to Use | When *Not* to Use |
|--------|-------------|-------------|-------------------|
| `os` | Interact with the operating system: file paths, env variables, processes. | File operations, cross-platform scripting. | Low-level system calls. |
| `sys` | System-specific parameters and functions like `sys.argv`, `sys.path`. | Script entry points, command-line tools. | Avoid for complex argument parsing (use `argparse`). |
| `socket` | Low-level networking interface. | TCP/UDP socket programming. | High-level HTTP APIs. |
| `subprocess` | Run and manage external processes. | Call shell commands from Python. | Avoid for direct file manipulation. |
| `platform` | Access system-specific information (OS, architecture). | OS-dependent logic or logging. | Avoid frequent runtime checks. |
| `time` | Time-related functions (`sleep`, timestamps). | Delays, measuring time. | Use `datetime` or `schedule` for calendar-time logic. |
| `psutil` | Process and system monitoring (CPU, RAM, battery). | Performance monitoring, dashboards. | Not needed for static scripts. |
| `uuid` | Generate universally unique IDs. | File naming, session IDs. | Avoid for cryptographic guarantees. |
| `re` | Regular expressions for pattern matching. | Text cleaning, validation. | Avoid for structured formats like JSON/XML. |
| `json` | Encode/decode JSON. | API parsing, config files. | Use `pickle` or `yaml` for more complex types. |
| `mss` | Fast screen capturing (multi-platform). | Screen recording/snapshot tools. | Avoid for headless/server-only environments. |
| `fitz` (`PyMuPDF`) | Read/write PDF files efficiently. | Text/image extraction from PDFs. | Avoid for OCR-heavy tasks (use `pytesseract`). |
| `requests` | HTTP client for making web requests. | APIs, downloading files. | Avoid for heavy concurrent loads (use `httpx`, `aiohttp`). |

---

##  Machine Learning / Deep Learning

| Library | Description | When to Use | When *Not* to Use |
|--------|-------------|-------------|-------------------|
| `numpy` | Base for numerical computing (arrays, vector ops). | Core of most ML pipelines. | Use `pandas` for tabular data. |
| `pandas` | Data manipulation and analysis. | Tabular data, CSVs, data cleaning. | Avoid for large-scale parallel data (use `dask`). |
| `scikit-learn` | Classical ML: regression, classification, clustering. | Quick baselines, student projects. | Not for deep learning (use PyTorch/TensorFlow). |
| `matplotlib` / `seaborn` | Visualization libraries. | Exploratory data analysis. | For interactive/dynamic plots, prefer `plotly`. |
| `plotly` | Interactive, browser-based plots. | Dashboards, Jupyter notebooks. | For static plots, `matplotlib` is faster. |
| `torch` (PyTorch) | Deep learning framework. | Custom DL models, research. | Use TensorFlow/Keras for production scalability. |
| `tensorflow` + `keras` | DL framework with high-level API. | Training, deployment. | Use PyTorch for more flexibility. |
| `optuna` | Hyperparameter optimization. | Auto-tuning ML/DL models. | Overkill for small models. |
| `joblib` | Fast parallel computing and caching. | Scikit-learn pipelines, multiprocessing. | Avoid for GPU-heavy tasks. |
| `tqdm` | Progress bars for loops. | Long-running scripts. | Not needed in quick batch scripts. |
| `lightgbm` | Fast gradient boosting framework. | Tabular data, Kaggle competitions. | Avoid for image/text data. |
| `xgboost` | Powerful ensemble method. | Structured data, small datasets. | Avoid for unstructured tasks. |
| `sentence-transformers` | Easy-to-use transformer embeddings. | Text similarity, semantic search. | Not needed for classic ML. |

---

##  Web / Visualization / Networking

| Library | Description | When to Use | When *Not* to Use |
|--------|-------------|-------------|-------------------|
| `streamlit` | Build interactive UIs for ML/web apps. | Quick prototypes, dashboards. | For full frontend apps, use React/Flask. |
| `dash` | Web-based analytical apps (built on Plotly). | Data apps with callbacks. | Avoid for large UIs or REST APIs. |
| `flask` / `fastapi` | Lightweight web frameworks. | API backend, deployment. | Avoid for complex frontend logic. |
| `gradio` | Fast web UIs for ML models. | Model sharing demos. | Less customizable than Streamlit. |
| `beautifulsoup4` | HTML parsing and scraping. | Web scraping. | Not ideal for JavaScript-heavy pages. |
| `aiohttp` | Async web requests. | Concurrent HTTP APIs. | Use `requests` for sync jobs. |

---

##  Graphs, Math & Utilities

| Library | Description | When to Use | When *Not* to Use |
|--------|-------------|-------------|-------------------|
| `networkx` | Create, manipulate, and visualize graphs. | Social networks, graph algorithms. | Avoid for large graphs (use `igraph`). |
| `sympy` | Symbolic math in Python. | Calculus, algebra, equations. | Use `numpy` for numerical math. |
| `numba` | Just-in-time compilation to speed up numpy code. | Speeding up math-heavy loops. | Not useful for GPU/ML tasks. |
| `cython` | Compile Python to C for speed. | Performance-critical code. | Increases build complexity. |
| `pydantic` | Data validation using Python types. | Robust API inputs, config validation. | Avoid for plain scripts. |
| `typing` | Type hints for Python. | Static type checking. | Optional, but improves code quality. |
| `rich` | Render beautiful terminal output. | Logs, markdown, progress bars. | Not needed in minimal scripts. |
| `loguru` | Simplified logging. | Cleaner logs. | Avoid when default `logging` suffices. |

---

##  Others Worth Exploring

| Library | Description | Use Case |
|--------|-------------|----------|
| `hydra` | Hierarchical config manager (great for ML). | ML experiments with many parameters. |
| `wandb` | ML experiment tracking. | Training logs, visualizations, comparisons. |
| `dvc` | Version control for datasets and models. | Team-based ML projects. |
| `openpyxl` | Excel spreadsheet reader/writer. | Reading/writing `.xlsx` files. |
| `schedule` | Python job scheduler (like cron). | Background scripts, automation. |
| `pyyaml` | YAML parser. | Config files with nesting. |

---



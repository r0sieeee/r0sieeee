### Biomedical Engineering @ UBC · building clinical AI

**EchoMCP** · UBC Robotics & Control Lab · *code is in private lab repos*
An LLM agent that answers clinical questions about echocardiograms.
- **RAG layer:** ~2,500 passages from 10 ASE cardiology guidelines, indexed with FAISS + MedCPT embeddings and exposed as an MCP tool (FastMCP, Ollama), so every answer cites its society, year and page
- **Table extraction:** PyMuPDF plus dual-representation chunking (text for search, labelled cells for the model)
- **Evaluation:** automated harness scored against a 57-metric clinical ground truth, with unit-aware scoring and an LLM-as-judge pass; runs as SLURM batch jobs on a GPU cluster
- **Finding:** the failing metrics failed on every model, from a 1.7B general LLM to a domain-tuned medical model. The bottleneck was table retrieval, not model size
- **Serving:** wrapped the team's echo models as MCP tools on NVIDIA Triton (B300 GPU cluster, Apptainer, AWS S3)

**Case Closed** · public · solo hackathon build
Autonomous LLM detective agent in Python using Gemini API tool calling. Deterministic code handles state, movement and alibi timelines, and the LLM handles judgement calls. Finished 0.046 points off the podium.

**UBC Rover · Science subteam** · *code is in the team's private repos*
Visible-light spectrophotometer for the rover's life-detection tests.
- **Acquisition:** detector and sensor modules integrated with a Raspberry Pi for real-time signal capture
- **Calibration:** Python curve-fitting that converts raw detector readings into absorbance, using calibrated white-light sources and optical filters with defined emission spectra
- **Visualization:** Python plots for checking calibration and sample readings

**Stack:** Python · PyTorch · Java · C · FAISS · MCP · RAG · NVIDIA Triton · SLURM · Apptainer · Raspberry Pi · Linux · Git

Happy to walk through the private work on request.

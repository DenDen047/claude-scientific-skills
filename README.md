# Claude Scientific Skills

> **New: [K-Dense BYOK](https://github.com/K-Dense-AI/k-dense-byok)** — A free, open-source AI co-scientist that runs on your desktop, powered by Claude Scientific Skills. Bring your own API keys, pick from 40+ models, and get a full research workspace with web search, file handling, 250+ scientific databases, and access to all 170+ skills in this repo. Your data stays on your computer, and you can optionally scale to cloud compute via [Modal](https://modal.com/) for heavy workloads. [Get started here.](https://github.com/K-Dense-AI/k-dense-byok)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE.md)
[![Skills](https://img.shields.io/badge/Skills-85-brightgreen.svg)](#whats-included)
[![Agent Skills](https://img.shields.io/badge/Standard-Agent_Skills-blueviolet.svg)](https://agentskills.io/)
[![Works with](https://img.shields.io/badge/Works_with-Cursor_|_Claude_Code_|_Codex-blue.svg)](#getting-started)
[![X](https://img.shields.io/badge/Follow_on_X-%40k__dense__ai-000000?logo=x)](https://x.com/k_dense_ai)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-K--Dense_Inc.-0A66C2?logo=linkedin)](https://www.linkedin.com/company/k-dense-inc)
[![YouTube](https://img.shields.io/badge/YouTube-K--Dense_Inc.-FF0000?logo=youtube)](https://www.youtube.com/@K-Dense-Inc)

A curated collection of **85 scientific and research skills** for any AI agent that supports the open [Agent Skills](https://agentskills.io/) standard, originally created by [K-Dense](https://k-dense.ai). Works with **Cursor, Claude Code, Codex, and more**. This fork is tailored for **computer science, machine learning, data science, and general research workflows** — biology/medical-specific skills have been removed to reduce context overhead.

<p align="center">
  <a href="https://k-dense.ai">
    <img src="docs/k-dense-web.gif" alt="K-Dense Web Demo" width="800"/>
  </a>
  <br/>
  <em>The demo above shows <a href="https://k-dense.ai">K-Dense Web</a> — the hosted platform built on top of these skills. Claude Scientific Skills is the open-source skill collection; K-Dense Web is the full AI co-scientist platform with more power and zero setup.</em>
</p>

---

These skills enable your AI agent to seamlessly work with specialized libraries, databases, and tools. While the agent can use any Python package or API on its own, these explicitly defined skills provide curated documentation and examples that make it significantly stronger and more reliable for the workflows below:
- 🤖 Machine Learning & AI - Deep learning, reinforcement learning, time series analysis, model interpretability, Bayesian methods
- 📊 Data Analysis & Visualization - Statistical analysis, network analysis, time series, publication-quality figures, large-scale data processing, EDA
- 🔮 Materials Science & Physics - Crystal structure analysis, quantum computing, symbolic mathematics, physics computations
- 🌌 Astronomy - Astronomical data analysis, coordinate transformations, cosmological calculations
- ⚙️ Engineering & Simulation - Discrete-event simulation, multi-objective optimization, systems modeling, computational fluid dynamics
- 🌍 Geospatial Science - GIS analysis, spatial statistics, remote sensing, machine learning for Earth observation
- 📚 Scientific Communication - Literature review, peer review, scientific writing, document processing, posters, slides, schematics, citation management
- 🎓 Research Methodology - Hypothesis generation, scientific brainstorming, critical thinking, grant writing, scholar evaluation
- 💹 Financial & Economic Data - SEC filings, macroeconomic data, market data, hedge fund analytics

**Transform your AI coding agent into an 'AI Scientist' on your desktop!**

> ⭐ **If you find this repository useful**, please consider giving it a star! It helps others discover these tools and encourages us to continue maintaining and expanding this collection.

> 🎬 **New to Claude Scientific Skills?** Watch our [Getting Started with Claude Scientific Skills](https://youtu.be/ZxbnDaD_FVg) video for a quick walkthrough.

---

## 📦 What's Included

This repository provides **85 scientific and research skills** organized into the following categories:

- **30+ Optimized Python Package Skills** - PyTorch Lightning, scikit-learn, Transformers, PennyLane, Qiskit, NetworkX, Polars, Dask, and others — with curated documentation, examples, and best practices
- **10+ Database & Data Source Skills** - OpenAlex, PubMed, bioRxiv, arXiv, FRED, Alpha Vantage, SEC EDGAR, and more
- **30+ Analysis & Communication Tools** - Literature review, scientific writing, peer review, document processing, posters, slides, schematics, infographics, Mermaid diagrams, and more
- **10+ Research Methodology Tools** - Hypothesis generation, grant writing, statistical analysis, EDA, scholar evaluation

Each skill includes:
- ✅ Comprehensive documentation (`SKILL.md`)
- ✅ Practical code examples
- ✅ Use cases and best practices
- ✅ Integration guides
- ✅ Reference materials

---

## 📋 Table of Contents

- [What's Included](#whats-included)
- [Why Use This?](#why-use-this)
- [Getting Started](#getting-started)
- [Support Open Source](#-support-the-open-source-community)
- [Prerequisites](#prerequisites)
- [Quick Examples](#quick-examples)
- [Use Cases](#use-cases)
- [Available Skills](#available-skills)
- [Contributing](#contributing)
- [Troubleshooting](#troubleshooting)
- [FAQ](#faq)
- [Support](#support)
- [Join Our Community](#join-our-community)
- [Citation](#citation)
- [License](#license)

---

## 🚀 Why Use This?

### ⚡ **Accelerate Your Research**
- **Save Days of Work** - Skip API documentation research and integration setup
- **Production-Ready Code** - Tested, validated examples following scientific best practices
- **Multi-Step Workflows** - Execute complex pipelines with a single prompt

### 🎯 **Focused Coverage**
- **85 Skills** - Focused on CS, ML, data science, and general research workflows
- **30+ Python Package Skills** - PyTorch Lightning, scikit-learn, Transformers, PennyLane, Qiskit, NetworkX, Polars, Dask, and others
- **10+ Database Skills** - OpenAlex, PubMed, bioRxiv, arXiv, FRED, Alpha Vantage, and more

### 🔧 **Easy Integration**
- **Simple Setup** - Copy skills to your skills directory and start working
- **Automatic Discovery** - Your agent automatically finds and uses relevant skills
- **Well Documented** - Each skill includes examples, use cases, and best practices

### 🌟 **Maintained & Supported**
- **Regular Updates** - Continuously maintained and expanded by K-Dense team
- **Community Driven** - Open source with active community contributions
- **Enterprise Ready** - Commercial support available for advanced needs

---

## 🎯 Getting Started

### Option A: Install via Claude Code Plugin (Recommended for Claude Code users)

Run the following commands in Claude Code:

```shell
/plugin marketplace add DenDen047/claude-scientific-skills
/plugin install scientific-skills
```

### Option B: Manual Installation

Claude Scientific Skills follows the open [Agent Skills](https://agentskills.io/) standard. Simply copy the skill folders into your skills directory and your AI agent will automatically discover and use them.

#### Step 1: Clone the Repository

```bash
git clone https://github.com/K-Dense-AI/claude-scientific-skills.git
```

#### Step 2: Copy Skills to Your Skills Directory

Copy the individual skill folders from `scientific-skills/` to one of the supported skill directories below. You can install skills **globally** (available across all projects) or **per-project** (available only in that project).

**Global installation** (recommended — skills available everywhere):

| Tool | Directory |
|------|-----------|
| Cursor | `~/.cursor/skills/` |
| Claude Code | `~/.claude/skills/` |
| Codex | `~/.codex/skills/` |
| Gemini CLI | `~/.gemini/skills/` |

**Project-level installation** (skills scoped to a single project):

| Tool | Directory |
|------|-----------|
| Cursor | `.cursor/skills/` (in your project root) |
| Claude Code | `.claude/skills/` (in your project root) |
| Codex | `.codex/skills/` (in your project root) |
| Gemini CLI | `.gemini/skills/` (in your project root) |

> **Note:** Cursor also reads from `.claude/skills/`, `.codex/skills/`, and `.gemini/skills/` directories, and vice versa, so skills are cross-compatible between tools.

**Example — global install for Cursor:**
```bash
cp -r claude-scientific-skills/scientific-skills/* ~/.cursor/skills/
```

**Example — global install for Claude Code:**
```bash
cp -r claude-scientific-skills/scientific-skills/* ~/.claude/skills/
```

**Example — global install for Gemini CLI:**
```bash
cp -r claude-scientific-skills/scientific-skills/* ~/.gemini/skills/
```

**Example — project-level install:**
```bash
mkdir -p .cursor/skills
cp -r /path/to/claude-scientific-skills/scientific-skills/* .cursor/skills/
```

**That's it!** Your AI agent will automatically discover the skills and use them when relevant to your scientific tasks. You can also invoke any skill manually by mentioning the skill name in your prompt.

---

## ❤️ Support the Open Source Community

Claude Scientific Skills is powered by many incredible open source projects maintained by dedicated developers and research communities worldwide. Projects like scikit-learn, PyTorch Lightning, NetworkX, Polars, and many others form the foundation of these skills.

**If you find value in this repository, please consider supporting the projects that make it possible:**

- ⭐ **Star their repositories** on GitHub
- 💰 **Sponsor maintainers** via GitHub Sponsors or NumFOCUS
- 📝 **Cite projects** in your publications
- 💻 **Contribute** code, docs, or bug reports

👉 **[View the full list of projects to support](docs/open-source-sponsors.md)**

---

## ⚙️ Prerequisites

- **Python**: 3.9+ (3.12+ recommended for best compatibility)
- **uv**: Python package manager (required for installing skill dependencies)
- **Client**: Any agent that supports the [Agent Skills](https://agentskills.io/) standard (Cursor, Claude Code, Gemini CLI, Codex, etc.)
- **System**: macOS, Linux, or Windows with WSL2
- **Dependencies**: Automatically handled by individual skills (check `SKILL.md` files for specific requirements)

### Installing uv

The skills use `uv` as the package manager for installing Python dependencies. Install it using the instructions for your operating system:

**macOS and Linux:**
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows:**
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

**Alternative (via pip):**
```bash
pip install uv
```

After installation, verify it works by running:
```bash
uv --version
```

For more installation options and details, visit the [official uv documentation](https://docs.astral.sh/uv/).

---

## 💡 Quick Examples

Once you've installed the skills, you can ask your AI agent to execute complex multi-step scientific workflows. Here are some example prompts:

### 🤖 ML Research Pipeline
**Goal**: Build and evaluate a graph neural network for citation network analysis

**Prompt**:
```
Use available skills you have access to whenever possible. Load the Cora citation dataset with
Torch Geometric, build a GCN model with PyTorch Lightning, evaluate with scikit-learn metrics,
interpret predictions with SHAP, search OpenAlex for related methods papers, and create
publication-quality visualizations with matplotlib and seaborn.
```

**Skills Used**: Torch Geometric, PyTorch Lightning, scikit-learn, SHAP, OpenAlex, matplotlib, seaborn, scientific visualization

---

### 📊 Time Series Forecasting & Analysis
**Goal**: Forecast economic indicators with multiple approaches

**Prompt**:
```
Use available skills you have access to whenever possible. Pull GDP and unemployment data from
FRED, apply zero-shot forecasting with TimesFM, compare against classical methods using aeon
and statsmodels, perform Bayesian modeling with PyMC, visualize results with Plotly, and write
up findings with scientific writing tools.
```

**Skills Used**: FRED, TimesFM, aeon, statsmodels, PyMC, Plotly, scientific writing

---

### 🌍 Geospatial Data Science
**Goal**: Analyze urban heat island effects using satellite and census data

**Prompt**:
```
Use available skills you have access to whenever possible. Load satellite-derived land surface
temperature with GeoMaster, join with census tract data via GeoPandas, perform spatial
statistics and clustering, build a predictive model with scikit-learn, create interactive
maps with Plotly, and generate an infographic summarizing key findings.
```

**Skills Used**: GeoMaster, GeoPandas, scikit-learn, Plotly, infographics, scientific visualization

> 📖 **Want more examples?** Check out [docs/examples.md](docs/examples.md) for comprehensive workflow examples and detailed use cases across all scientific domains.

---

## 🚀 Want to Skip the Setup and Just Do the Science?

**Recognize any of these?**

- You spent more time configuring environments than running analyses
- Your workflow needs a GPU your local machine does not have
- You need a shareable, publication-ready figure or report, not just a script
- You want to run a complex multi-step pipeline right now, without reading package docs first

If so, **[K-Dense Web](https://k-dense.ai)** was built for you. It is the full AI co-scientist platform: everything in this repo plus cloud GPUs, 200+ skills, and outputs you can drop directly into a paper or presentation. Zero setup required.

| Feature | This Repo | K-Dense Web |
|---------|-----------|-------------|
| Scientific Skills | 85 skills (CS-focused) | **200+ skills** (all domains) |
| Setup | Manual installation | **Zero setup, works instantly** |
| Compute | Your machine | **Cloud GPUs and HPC included** |
| Workflows | Prompt and code | **End-to-end research pipelines** |
| Outputs | Code and analysis | **Publication-ready figures, reports, and papers** |
| Integrations | Local tools | **Lab systems, ELNs, and cloud storage** |

> *"K-Dense Web took me from raw sequencing data to a draft figure in one afternoon. What used to take three days of environment setup and scripting now just works."*
> **Computational biologist, drug discovery**

> ### 💰 $50 in free credits, no credit card required
> Start running real scientific workflows in minutes.
>
> **[Try K-Dense Web free](https://k-dense.ai)**

*[k-dense.ai](https://k-dense.ai) | [Read the full comparison](https://k-dense.ai/blog/k-dense-web-vs-claude-scientific-skills)*

---

## 🔬 Use Cases

### 🤖 Machine Learning & AI
- **Deep Learning**: Build and train models with PyTorch Lightning, Transformers, Torch Geometric
- **Classical ML**: Classification, regression, clustering with scikit-learn, survival analysis with scikit-survival
- **Reinforcement Learning**: Train RL agents with Stable Baselines3 and PufferLib
- **Model Interpretability**: Explain predictions with SHAP, reduce dimensionality with UMAP
- **Time Series**: Forecasting, classification, anomaly detection with aeon and TimesFM

### 📊 Data Analysis & Visualization
- **Statistical Analysis**: Hypothesis testing, power analysis, experimental design with statsmodels and PyMC
- **Publication Figures**: Create publication-quality visualizations with matplotlib, seaborn, and Plotly
- **Network Analysis**: Analyze and visualize complex networks with NetworkX
- **Large-Scale Data**: Process larger-than-RAM datasets with Dask, Polars, and Vaex
- **Report Generation**: Generate comprehensive PDF, DOCX, PPTX reports with Document Skills

### 🌍 Geospatial Science
- **GIS Analysis**: Spatial statistics, vector/raster data with GeoPandas and GeoMaster
- **Remote Sensing**: Satellite imagery processing, land use classification
- **Spatial ML**: Machine learning for Earth observation

### 🔮 Materials Science & Physics
- **Materials**: Crystal structure analysis with Pymatgen
- **Quantum Computing**: Circuit design and simulation with Cirq, PennyLane, Qiskit, QuTiP
- **Astronomy**: Data analysis and cosmological calculations with Astropy
- **Symbolic Math**: Algebraic manipulation and calculus with SymPy

### 💹 Financial & Economic Research
- **SEC Filings**: Analyze 10-K, 10-Q, insider trading with edgartools
- **Macroeconomic Data**: GDP, unemployment, inflation from FRED
- **Market Data**: Stocks, options, forex, crypto with Alpha Vantage
- **Fiscal Data**: U.S. Treasury data with usfiscaldata

---

## 📚 Available Skills

This repository contains **85 scientific and research skills** focused on CS, ML, data science, and general research workflows. Each skill provides comprehensive documentation, code examples, and best practices.

### Skill Categories

> **Note:** The skills listed below are *explicitly defined* — curated with documentation, examples, and best practices. The agent can install and use *any* Python package or call *any* API, even without a dedicated skill. The skills listed simply make common workflows faster and more dependable.

#### 🤖 **Machine Learning & AI** (16 skills)
- Deep learning: PyTorch Lightning, Transformers, Stable Baselines3, PufferLib
- Classical ML: scikit-learn, scikit-survival, SHAP
- Time series: aeon, TimesFM (Google's zero-shot foundation model)
- Bayesian methods: PyMC
- Optimization: PyMOO
- Graph ML: Torch Geometric
- Dimensionality reduction: UMAP-learn
- Statistical modeling: statsmodels
- Hypothesis discovery: HypoGeniC

#### 🔮 **Materials Science & Physics** (6 skills)
- Materials: Pymatgen
- Astronomy: Astropy
- Quantum computing: Cirq, PennyLane, Qiskit, QuTiP

#### ⚙️ **Engineering & Simulation** (6 skills)
- Numerical computing: MATLAB/Octave
- Computational fluid dynamics: FluidSim
- Discrete-event simulation: SimPy
- Data processing: Dask, Polars, Vaex

#### 📊 **Data Analysis & Visualization** (17 skills)
- Visualization: Matplotlib, Seaborn, Plotly, Scientific Visualization
- Geospatial: GeoPandas, GeoMaster
- Network analysis: NetworkX
- Symbolic math: SymPy
- Document processing: PDF, DOCX, PPTX, XLSX
- Infographics, Markdown & Mermaid Writing
- Data access: Data Commons
- EDA and Statistical Analysis workflows
- N-D arrays: Zarr

#### 📚 **Scientific Communication** (20 skills)
- Literature: OpenAlex, PubMed, bioRxiv, arXiv, Literature Review
- Advanced paper search: BGPT Paper Search
- Web search: Perplexity Search, Parallel Web
- Writing: Scientific Writing, Peer Review
- Document processing: XLSX, MarkItDown
- Publishing: Paper-2-Web, Venue Templates
- Presentations: Scientific Slides, LaTeX Posters, PPTX Posters
- Diagrams: Scientific Schematics, Markdown & Mermaid Writing
- Infographics, Citation Management
- Illustration: Generate Image

#### 🔬 **Databases & Data Sources** (10 skills)
- Literature: bioRxiv, arXiv, OpenAlex, PubMed
- Patents: USPTO
- Financial: FRED, Alpha Vantage, edgartools, usfiscaldata, hedgefundmonitor

#### 🔧 **Infrastructure & Platforms** (2 skills)
- Cloud compute: Modal
- Resource detection: Get Available Resources

#### 🎓 **Research Methodology & Planning** (8 skills)
- Ideation: Scientific Brainstorming, Hypothesis Generation
- Critical analysis: Scientific Critical Thinking, Scholar Evaluation
- Scenario analysis: What-If Oracle
- Multi-perspective deliberation: Consciousness Council
- Cognitive profiling: DHDNA Profiler
- Funding: Research Grants
- Discovery: Research Lookup
- Market analysis: Market Research Reports

#### 💹 **Financial & SEC Research** (5 skills)
- SEC filings: edgartools
- U.S. fiscal data: usfiscaldata
- Macroeconomic data: FRED
- Hedge fund analytics: hedgefundmonitor
- Global market data: Alpha Vantage

#### 🔧 **Utility** (2 skills)
- File-based planning: Planning with Files
- Reference management: pyzotero

> 📖 **For complete details on all skills**, see [docs/scientific-skills.md](docs/scientific-skills.md)

> 💡 **Looking for practical examples?** Check out [docs/examples.md](docs/examples.md) for comprehensive workflow examples across all scientific domains.

---

## 🤝 Contributing

We welcome contributions to expand and improve this scientific skills repository!

### Ways to Contribute

✨ **Add New Skills**
- Create skills for additional scientific packages or databases
- Add integrations for scientific platforms and tools

📚 **Improve Existing Skills**
- Enhance documentation with more examples and use cases
- Add new workflows and reference materials
- Improve code examples and scripts
- Fix bugs or update outdated information

🐛 **Report Issues**
- Submit bug reports with detailed reproduction steps
- Suggest improvements or new features

### How to Contribute

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-skill`)
3. **Follow** the existing directory structure and documentation patterns
4. **Ensure** all new skills include comprehensive `SKILL.md` files
5. **Test** your examples and workflows thoroughly
6. **Commit** your changes (`git commit -m 'Add amazing skill'`)
7. **Push** to your branch (`git push origin feature/amazing-skill`)
8. **Submit** a pull request with a clear description of your changes

### Contribution Guidelines

✅ **Adhere to the [Agent Skills Specification](https://agentskills.io/specification)** — Every skill must follow the official spec (valid `SKILL.md` frontmatter, naming conventions, directory structure)  
✅ Maintain consistency with existing skill documentation format  
✅ Ensure all code examples are tested and functional  
✅ Follow scientific best practices in examples and workflows  
✅ Update relevant documentation when adding new capabilities  
✅ Provide clear comments and docstrings in code  
✅ Include references to official documentation

### Security Scanning

All skills in this repository are security-scanned using [Cisco AI Defense Skill Scanner](https://github.com/cisco-ai-defense/skill-scanner), an open-source tool that detects prompt injection, data exfiltration, and malicious code patterns in Agent Skills.

If you are contributing a new skill, we recommend running the scanner locally before submitting a pull request:

```bash
uv pip install cisco-ai-skill-scanner
skill-scanner scan /path/to/your/skill --use-behavioral
```

> **Note:** A clean scan result reduces noise in review, but does not guarantee a skill is free of all risk. Contributed skills are also reviewed manually before merging.

### Recognition

Contributors are recognized in our community and may be featured in:
- Repository contributors list
- Special mentions in release notes
- K-Dense community highlights

Your contributions help make scientific computing more accessible and enable researchers to leverage AI tools more effectively!

### Support Open Source

This project builds on 50+ amazing open source projects. If you find value in these skills, please consider [supporting the projects we depend on](docs/open-source-sponsors.md).

---

## 🔧 Troubleshooting

### Common Issues

**Problem: Skills not loading**
- Verify skill folders are in the correct directory (see [Getting Started](#getting-started))
- Each skill folder must contain a `SKILL.md` file
- Restart your agent/IDE after copying skills
- In Cursor, check Settings → Rules to confirm skills are discovered

**Problem: Missing Python dependencies**
- Solution: Check the specific `SKILL.md` file for required packages
- Install dependencies: `uv pip install package-name`

**Problem: API rate limits**
- Solution: Many databases have rate limits. Review the specific database documentation
- Consider implementing caching or batch requests

**Problem: Authentication errors**
- Solution: Some services require API keys. Check the `SKILL.md` for authentication setup
- Verify your credentials and permissions

**Problem: Outdated examples**
- Solution: Report the issue via GitHub Issues
- Check the official package documentation for updated syntax

---

## ❓ FAQ

### General Questions

**Q: Is this free to use?**  
A: Yes! This repository is MIT licensed. However, each individual skill has its own license specified in the `license` metadata field within its `SKILL.md` file—be sure to review and comply with those terms.

**Q: Why are all skills grouped together instead of separate packages?**  
A: We believe good science in the age of AI is inherently interdisciplinary. Bundling all skills together makes it trivial for you (and your agent) to bridge across fields—e.g., combining genomics, cheminformatics, clinical data, and machine learning in one workflow—without worrying about which individual skills to install or wire together.

**Q: Can I use this for commercial projects?**  
A: The repository itself is MIT licensed, which allows commercial use. However, individual skills may have different licenses—check the `license` field in each skill's `SKILL.md` file to ensure compliance with your intended use.

**Q: Do all skills have the same license?**  
A: No. Each skill has its own license specified in the `license` metadata field within its `SKILL.md` file. These licenses may differ from the repository's MIT License. Users are responsible for reviewing and adhering to the license terms of each individual skill they use.

**Q: How often is this updated?**  
A: We regularly update skills to reflect the latest versions of packages and APIs. Major updates are announced in release notes.

**Q: Can I use this with other AI models?**  
A: The skills follow the open [Agent Skills](https://agentskills.io/) standard and work with any compatible agent, including Cursor, Claude Code, and Codex.

### Installation & Setup

**Q: Do I need all the Python packages installed?**  
A: No! Only install the packages you need. Each skill specifies its requirements in its `SKILL.md` file.

**Q: What if a skill doesn't work?**  
A: First check the [Troubleshooting](#troubleshooting) section. If the issue persists, file an issue on GitHub with detailed reproduction steps.

**Q: Do the skills work offline?**  
A: Database skills require internet access to query APIs. Package skills work offline once Python dependencies are installed.

### Contributing

**Q: Can I contribute my own skills?**  
A: Absolutely! We welcome contributions. See the [Contributing](#contributing) section for guidelines and best practices.

**Q: How do I report bugs or suggest features?**  
A: Open an issue on GitHub with a clear description. For bugs, include reproduction steps and expected vs actual behavior.

---

## 💬 Support

Need help? Here's how to get support:

- 📖 **Documentation**: Check the relevant `SKILL.md` and `references/` folders
- 🐛 **Bug Reports**: [Open an issue](https://github.com/K-Dense-AI/claude-scientific-skills/issues)
- 💡 **Feature Requests**: [Submit a feature request](https://github.com/K-Dense-AI/claude-scientific-skills/issues/new)
- 💼 **Enterprise Support**: Contact [K-Dense](https://k-dense.ai/) for commercial support
- 🌐 **Community**: [Join our Slack](https://join.slack.com/t/k-densecommunity/shared_invite/zt-3iajtyls1-EwmkwIZk0g_o74311Tkf5g)

---

## 🎉 Join Our Community!

**We'd love to have you join us!** 🚀

Connect with other scientists, researchers, and AI enthusiasts using AI agents for scientific computing. Share your discoveries, ask questions, get help with your projects, and collaborate with the community!

🌟 **[Join our Slack Community](https://join.slack.com/t/k-densecommunity/shared_invite/zt-3iajtyls1-EwmkwIZk0g_o74311Tkf5g)** 🌟

Whether you're just getting started or you're a power user, our community is here to support you. We share tips, troubleshoot issues together, showcase cool projects, and discuss the latest developments in AI-powered scientific research.

**See you there!** 💬

---

## 📖 Citation

If you use Claude Scientific Skills in your research or project, please cite it as:

### BibTeX
```bibtex
@software{claude_scientific_skills_2026,
  author = {{K-Dense Inc.}},
  title = {Claude Scientific Skills: A Comprehensive Collection of Scientific Tools for Claude AI},
  year = {2026},
  url = {https://github.com/K-Dense-AI/claude-scientific-skills},
  note = {85 skills covering ML, data science, and general research tools}
}
```

### APA
```
K-Dense Inc. (2026). Claude Scientific Skills: A comprehensive collection of scientific tools for Claude AI [Computer software]. https://github.com/K-Dense-AI/claude-scientific-skills
```

### MLA
```
K-Dense Inc. Claude Scientific Skills: A Comprehensive Collection of Scientific Tools for Claude AI. 2026, github.com/K-Dense-AI/claude-scientific-skills.
```

### Plain Text
```
Claude Scientific Skills by K-Dense Inc. (2026)
Available at: https://github.com/K-Dense-AI/claude-scientific-skills
```

We appreciate acknowledgment in publications, presentations, or projects that benefit from these skills!

---

## 📄 License

This project is licensed under the **MIT License**.

**Copyright © 2026 K-Dense Inc.** ([k-dense.ai](https://k-dense.ai/))

### Key Points:
- ✅ **Free for any use** (commercial and noncommercial)
- ✅ **Open source** - modify, distribute, and use freely
- ✅ **Permissive** - minimal restrictions on reuse
- ⚠️ **No warranty** - provided "as is" without warranty of any kind

See [LICENSE.md](LICENSE.md) for full terms.

### Individual Skill Licenses

> ⚠️ **Important**: Each skill has its own license specified in the `license` metadata field within its `SKILL.md` file. These licenses may differ from the repository's MIT License and may include additional terms or restrictions. **Users are responsible for reviewing and adhering to the license terms of each individual skill they use.**

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=K-Dense-AI/claude-scientific-skills&type=date&legend=top-left)](https://www.star-history.com/#K-Dense-AI/claude-scientific-skills&type=date&legend=top-left)

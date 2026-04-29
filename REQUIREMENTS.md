chemMind
├── Requirements and Dependencies
└── Last updated: 2026-04-28

1. Core LLM Frameworks
────────────────────────────────────────

langchain==0.3.20
  → LLM chaining, agents, tool integration
    
langchain-anthropic==0.3.10
  → Anthropic Claude API integration
    
langchain-openai==0.3.1
  → OpenAI GPT API integration
    
langchain-community==0.3.19
  → Community plugins (serpa, etc.)
    

2. Vector Database and Embeddings
────────────────────────────────────────

chromadb==0.6.3
  → Local vector database for RAG
    
sentence-transformers==3.3.1
  → Text embedding models (all-MiniLM-L6-v2)
    

3. Chemical Informatics
────────────────────────────────────────

rdkit-pypi==2024.9.6
  → Chemical structure handling (SMILES, InChI, MOL)
    
openbabel-wheel==3.1.1.1
  → Chemical file format conversion
    

4. PDF Processing
────────────────────────────────────────

PyMuPDF==1.25.3
  → Fast PDF text extraction (fitz module)
    
pdfplumber==0.11.4
  → PDF table extraction, bounding box analysis
    

5. Document Generation
────────────────────────────────────────

python-docx==1.1.2
  → Word (.docx) generation and editing
    
matplotlib==3.10.1
  → Publication-quality plot generation
    

6. Materials Science
────────────────────────────────────────

pymatgen==2025.2.10
  → Materials analysis (band gap, DOS, etc.)
    
ase==3.24.0
  → Atomic Simulation Environment (VASP, Gaussian interfaces)
    

7. Utilities
────────────────────────────────────────

pyyaml==6.0.2
  → YAML configuration file parsing
    
python-dotenv==1.0.1
  → Environment variable loading (.env files)
    
tqdm==4.67.1
  → Progress bar for long operations
    

8. Development Tools (Optional)
────────────────────────────────────────

jupyter==1.0.0
  → Jupyter Notebook support
    
pytest==8.2.1
  → Unit testing framework
    
black==24.4.2
  → Code formatter
    

9. Installation
────────────────────────────────────────

# Create virtual environment (recommended)
python -m venv venv

# Activate (Windows)
venv\Scripts\activate

# Activate (Linux/Mac)
source venv/bin/activate

# Install all dependencies
pip install -r requirements.txt

10. Hardware Requirements
────────────────────────────────────────

Minimum:
  → CPU: 4 cores
  → RAM: 8 GB
  → Disk: 5 GB (incl. dependencies)
  → GPU: Not required

Recommended:
  → CPU: 8 cores
  → RAM: 16 GB
  → Disk: 10 GB SSD
  → GPU: Optional (for local LLM)

11. API Keys Required
────────────────────────────────────────

Anthropic API Key:
  → Get from: https://console.anthropic.com/
  → Set in .env: ANTHROPIC_API_KEY=sk-ant-...
    
OpenAI API Key (optional):
  → Get from: https://platform.openai.com/
  → Set in .env: OPENAI_API_KEY=sk-...
    
MiMo API Key (coming soon):
  → Get from: https://100t.xiaomimimo.com/
  → Set in .env: MIMO_API_KEY=...
    

12. Verified Environment
────────────────────────────────────────

OS: Windows 11 23H2
Python: 3.12.4
IDE: PyCharm Professional 2024.3
RAM: 16 GB
CPU: Intel i7-12700H

13. Dependency Tree (Simplified)
────────────────────────────────────────

chemMind
├── langchain (0.3.20)
│   ├── langchain-core (≥0.3.20)
│   ├── langchain-anthropic (0.3.10)
│   └── langchain-openai (0.3.1)
├── chromadb (0.6.3)
│   ├── sentence-transformers (3.3.1)
│   └── numpy (≥1.25.0)
├── rdkit-pypi (2024.9.6)
├── PyMuPDF (1.25.3)
├── python-docx (1.1.2)
└── pymatgen (2025.2.10)
    ├── numpy (≥1.25.0)
    └── pandas (≥2.0.0)

14. Common Installation Issues
────────────────────────────────────────

Issue 1: rdkit installation fails (Windows)
Solution: Use rdkit-pypi instead of rdkit
    
Issue 2: PyMuPDF import error
Solution: Install with pip install --upgrade pip
    
Issue 3: chromadb hangs on first run
Solution: Wait 5-10 min (downloads embedding model)
    

15. Version Pinning Strategy
────────────────────────────────────────

We pin major versions (e.g., langchain==0.3.20) to ensure:
  ✓ Reproducible builds
  ✓ No breaking API changes
  ✓ Compatible dependency tree
    
For development, you may use >= instead:
  langchain>=0.3.20

16. License Compliance Check
────────────────────────────────────────

✓ langchain: MIT License (commercial use OK)
✓ chromadb: Apache 2.0 (commercial use OK)
✓ rdkit: BSD-3-Clause (commercial use OK)
✓ PyMuPDF: AGPL-3.0 (needs care for commercial use)
  
⚠️ PyMuPDF License Note:
   If you plan to commercialize ChemMind, consider:
   → Purchasing a commercial PyMuPDF license, or
   → Switching to pdfplumber (BSD license)

17. Contact
────────────────────────────────────────

For dependency issues:
  → Open a GitHub Issue: https://github.com/A-Duck1/chemmind/issues
  → Or email: chem.mind.project@gmail.com

────────────────────────────────────────
End of Requirements Documentation
────────────────────────────────────────

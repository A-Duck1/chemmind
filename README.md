# chemmind
AI-driven chemistry learning and experiment design assistant
# ChemMind

[![Python](https://img.shields.io/badge/Python-3.12%2B-blue)](https://python.org)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> AI-driven chemistry learning and experiment design assistant

## Overview

ChemMind is an AI-powered assistant designed for chemistry students and researchers. It integrates Large Language Models (LLMs) with chemical informatics tools to provide intelligent literature analysis, synthesis route design, computational chemistry interpretation, and automated report generation.

## Features

### 1. ChemRAG - Intelligent Literature Assistant
- PDF parsing with chemical structure preservation
- Multi-level RAG architecture for literature retrieval
- Structured summarization of research papers
- Cross-paper knowledge integration

### 2. SynthFlow - Smart Synthesis Design
- Retrosynthetic analysis using BRICS algorithm
- LLM-driven reaction condition recommendations
- Safety assessment and reagent availability analysis
- Multi-route comparison and ranking

### 3. CompChem Interpreter - Computational Results Analysis
- Support for Materials Studio, VASP, Gaussian, and CP2K
- Band structure and DOS visualization
- Natural language interpretation of calculation results
- Automated report generation

### 4. AutoLab - Automated Report Generation
- Data cleaning and statistical analysis
- Automatic chart generation (Matplotlib/Plotly)
- Structured report output (Word/LaTeX)
- Professional formatting compliant with academic standards

## System Architecture

User Input Layer ↓ Core Processing Engine (LLM + RAG + Rule Engine) ↓ Knowledge Layer (ChemLit DB + Reaction DB + Spectral Lib) ↓ Output Generation Layer


## Quick Start

### Requirements
- Python 3.12+
- 8GB+ RAM (16GB recommended for long papers)

### Installation

```bash
# Clone repository
git clone https://github.com/A-Duck1/chemmind.git
cd chemmind

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Configure API keys
cp config.example.yaml config.yaml
# Edit config.yaml with your API keys
Usage Example
python
复制
from chemmind import ChemRAG

# Initialize ChemRAG
rag = ChemRAG()

# Analyze a chemistry paper
result = rag.analyze_paper("path/to/paper.pdf", mode="full_analysis")
print(result.summary)
print(result.structures)
Technology Stack
Core Framework: LangChain, LangGraph
LLM APIs: Anthropic Claude, OpenAI, MiMo (coming soon)
RAG Components: ChromaDB, Sentence-Transformers
Chemical Tools: RDKit, Open Babel
PDF Processing: PyMuPDF, pdfplumber
Document Generation: python-docx, LaTeX
Computational Chemistry: pymatgen, ASE
Token Usage
This project requires significant token consumption for:

Single paper processing: 50k-80k tokens (main text + SI)
Batch literature survey: 100k+ tokens (5-10 papers comparison)
Knowledge base construction: 300M+ tokens (1000 papers annotation)
Estimated 60-day requirement: ~800M tokens

Development Roadmap
Phase 1 (Completed)
 PDF parsing pipeline
 Word document auto-formatting engine
 Basic ChemRAG implementation
Phase 2 (In Progress)
 MiMo V2.5 integration (1M token context)
 ChemRAG knowledge base expansion (1000 papers)
 SynthFlow multi-step synthesis evaluation
Phase 3 (Planned)
 Web interface (Streamlit/Gradio)
 Multi-format computational chemistry support
 Community feedback integration
License
MIT License - see LICENSE for details.

Developer
Li Changxin

China University of Petroleum (East China)
Contact: 13398205591
Acknowledgments
Thanks to the open-source community for:

LangChain
RDKit
PyMuPDF
Materials Studio
Made with passion for chemistry and AI

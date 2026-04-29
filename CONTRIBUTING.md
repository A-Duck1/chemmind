# ChemMind - Contributing Guide

Thank you for your interest in contributing to ChemMind! This guide will help you get started.

## How to Contribute

### 1. Report Bugs

If you find a bug, please open an Issue with:
- **Description:** What went wrong?
- **Steps to reproduce:** How can we reproduce it?
- **Expected behavior:** What should happen?
- **Environment:** OS, Python version, etc.

**Issue template:**
```
Title: [BUG] Short description

Description:
Steps to reproduce:
1. 
2. 
3. 

Expected behavior:

Environment:
- OS: Windows 11 / Ubuntu 22.04 / macOS 14
- Python: 3.12.4
- ChemMind: v0.2.1
```

### 2. Suggest Features

Have an idea? Open an Issue with:
- **Title:** `[FEATURE] Feature name`
- **Description:** What should it do?
- **Use case:** Why is it useful?

### 3. Submit Pull Requests

#### Step 1: Fork & Clone

```bash
# Fork on GitHub, then clone your fork
git clone https://github.com/yourusername/chemmind.git
cd chemmind

# Add upstream
git remote add upstream https://github.com/A-Duck1/chemmind.git
```

#### Step 2: Create Branch

```bash
git checkout -b feature/your-feature-name
```

#### Step 3: Develop

- Write code
- Add tests
- Update documentation
- Test locally

```bash
# Run tests
pytest tests/

# Format code
black chemmind/

# Check linting
flynt chemmind/
```

#### Step 4: Commit

```bash
git add .
git commit -m "feat: add new feature"
```

**Commit message format:**
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation update
- `test:` Add tests
- `refactor:` Code refactoring

#### Step 5: Push & PR

```bash
git push origin feature/your-feature-name
```

Then open a Pull Request on GitHub.

---

## Development Setup

### 1. Clone & Install

```bash
git clone https://github.com/A-Duck1/chemmind.git
cd chemmind
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
pip install -r requirements-dev.txt  # dev dependencies
```

### 2. Configure API Keys

```bash
cp config.example.yaml config.yaml
# Edit config.yaml with your API keys
```

### 3. Run Tests

```bash
pytest tests/ -v
```

---

## Code Style

- Follow **PEP 8** (checked by `flynt`)
- Use **Black** for formatting (line length: 88)
- Add **type hints** (checked by `mypy`)
- Write **docstrings** (Google style)

**Example:**
```python
def analyze_paper(file_path: str, mode: str = "summary") -> Dict:
    """Analyze a chemistry paper.
    
    Args:
        file_path: Path to the PDF file.
        mode: Analysis mode ("summary", "full", "reactions").
        
    Returns:
        Dictionary with analysis results.
        
    Raises:
        FileNotFoundError: If file_path does not exist.
    """
    # implementation...
```

---

## Testing

- **Unit tests:** `tests/test_*.py`
- **Integration tests:** `tests/integration/`
- **Coverage:** Aim for >80%

**Run tests:**
```bash
# All tests
pytest

# With coverage
pytest --cov=chemmind

# Specific test file
pytest tests/test_chemrag.py -v
```

---

## Documentation

- **Docstrings:** All public functions/classes
- **README:** Update if adding user-facing features
- **Architecture:** Update `docs/architecture.md` for design changes

---

## Community

- **Be respectful:** Follow the [Code of Conduct](CODE_OF_CONDUCT.md)
- **Ask questions:** Open a Discussion on GitHub
- **Join Discord:** (coming soon)

---

## Recognition

Contributors will be recognized in:
- `README.md` (Contributors section)
- Release notes
- Project website (coming soon)

---

## Contact

- **Maintainer:** Li Changxin (lichenxin-chem)
- **Email:** chem.mind.project@gmail.com
- **GitHub Issues:** https://github.com/A-Duck1/chemmind/issues

---

**Thank you for contributing to ChemMind! 🎉**

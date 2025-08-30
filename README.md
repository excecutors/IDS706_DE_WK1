# IDS706_DE_WK1

# IDS706 Python Template Project

This repository is a starter template for the **Data Engineering Systems (IDS 706)** course. It demonstrates how to set up a Python project with testing, linting, formatting, and continuous integration using GitHub Actions.

---

## Project Overview
This project includes:
- A **Makefile** for common development tasks
- A **Python script** (`hello.py`) with simple functions
- **Unit tests** (`test_hello.py`) to ensure correctness
- A **requirements.txt** file for dependencies
- **GitHub Actions workflow** for automated testing and linting

---

## Repository Structure
```
IDS706_DE_WK1/
│-- hello.py              # Example Python code
│-- test_hello.py         # Unit tests
│-- Makefile              # Commands for build/test/format/lint
│-- requirements.txt      # Dependencies
│-- README.md             # Project documentation
│-- .github/workflows/    # GitHub Actions configuration
```

---

## Setup Instructions

### 1. Clone Repository
```bash
git clone https://github.com/<your-username>/IDS706_DE_WK1.git
cd IDS706_DE_WK1
```

### 2. Create Virtual Environment (Local Workflow)
```bash
python3 -m venv ~/.IDS706_python_template
source ~/.IDS706_python_template/bin/activate
```

### 3. Install Dependencies
```bash
make install
```

---

## Makefile Commands
| Command        | Description |
|----------------|-------------|
| `make install` | Install dependencies from `requirements.txt` |
| `make format`  | Format code using **Black** |
| `make lint`    | Check code style with **flake8** |
| `make test`    | Run tests with **pytest** and coverage |
| `make clean`   | Remove temporary/cache files |
| `make all`     | Run install, format, lint, and test |

---

## Example Code (`hello.py`)
```python
def say_hello(name: str) -> str:
    return f"Hello, {name}, welcome to Data Engineering Systems (IDS 706)!"


def add(a: int, b: int) -> int:
    return a + b
```

---

## Example Tests (`test_hello.py`)
```python
from hello import say_hello, add

def test_say_hello():
    assert say_hello("Annie") == "Hello, Annie, welcome to Data Engineering Systems (IDS 706)!"

def test_add():
    assert add(2, 3) == 5
```

---

## 🤖 GitHub Actions (CI/CD)
This project includes a workflow that:
- Installs dependencies
- Runs **flake8** for linting
- Runs **pytest** for testing

Workflow file: `.github/workflows/python.yml`

---

## How to Run
1. Run tests:
   ```bash
   make test
   ```
2. Format code:
   ```bash
   make format
   ```
3. Lint code:
   ```bash
   make lint
   ```

---

## Learning Objectives
- Practice setting up a Python development environment
- Use automation tools for linting, formatting, and testing
- Learn how GitHub Actions supports **Continuous Integration**
- Build a reusable template for future IDS 706 projects

---

## Author
Freddy Platinus  
Master of Engineering in Financial Technology, Duke University

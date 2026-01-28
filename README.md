# 🤖 Lerobot Dataset

A standalone version of [LerobotDataset](https://github.com/huggingface/lerobot/tree/main/src/lerobot/datasets) with relaxed dependencies for easier integration with other projects.

The `torch` and `torchvision` dependencies are deliberately omitted to allow you to manage your own PyTorch installation.

## 📦 Installation

### Prerequisites

- Python >= 3.10
- [uv](https://github.com/astral-sh/uv) package manager

### Setup

1. Install dependencies:
   ```bash
   uv sync
   ```

2. Install PyTorch:
   ```bash
   uv pip install torch torchvision --torch-backend=auto
   ```
   
   Or specify a backend:
   ```bash
   # For CUDA
   uv pip install torch torchvision --torch-backend=cuda
   
   # For CPU only
   uv pip install torch torchvision --torch-backend=cpu
   ```

3. Activate the virtual environment:
   ```bash
   source .venv/bin/activate
   ```

## 💻 Usage

```python
from ledataset.datasets.lerobot_dataset import LeRobotDataset

ds = LeRobotDataset("lerobot/pusht")

# Your code here
```

## 🔗 Related Projects

- [Lerobot](https://github.com/huggingface/lerobot) - Full Lerobot framework
- [LerobotDataset (Original)](https://github.com/huggingface/lerobot/tree/main/src/lerobot/datasets) - Original implementation

## 📝 License

See [LICENSE](LICENSE) file for details.

# Habit Tracker (Pixela API)

A habit tracking application developed as part of the "100 Days of Code: The Complete Python Pro Bootcamp". This tool allows users to track their daily reading progress by interacting with the Pixela API to create, update, and delete data points (pixels) on a visual activity graph.

## Getting Started

This project requires an internet connection to communicate with the Pixela API.

### Prerequisites
* Python 3.x installed.
* Requests library installed:
  ```bash
  pip install requests
  ```

### Setting Up Your Pixela Token
The Pixela token is **not** stored in the code. Set it as an environment variable before running the script:

```bash
export PIXELA_TOKEN="your_token_here"
python3 main.py
```

If the variable is missing, the script stops and tells you to set it.

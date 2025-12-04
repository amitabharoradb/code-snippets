```python
## Define an empty config object
```python
if 'config' not in locals():
  config = {}
```

```python
## How to call notebook at a different dir level
import sys, os

# Add the ../agent_eval path relative to current working directory
agent_eval_path = os.path.abspath(os.path.join(os.getcwd(), "../02-agent-eval"))
sys.path.append(agent_eval_path)
```
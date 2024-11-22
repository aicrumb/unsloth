i didn't like that despite only using a single gpu i couldn't run anything because "multi-gpu setups are not supported" 🤷‍♀️

the speedups are worth it as someone who is regularly working on a machine with only two gpus who likes to multi-task anyway (e.g. generate data or host model for inference otherwise on one gpu, finetune on the other) so i just replaced all the relavent error raising with print statements 👍

**installation**
```
pip install -U git+https://github.com/aicrumb/unsloth
```

**use**

before your trainer either

1. inside the script before anything else runs
```python
import os
os.environ['CUDA_VISIBLE_DEVICES'] = '0' # otherwise the gpu you'll run on
```
2. in the terminal
```
export CUDA_VISIBLE_DEVICES=0
```

check the [original repo](https://github.com/unslothai/unsloth) or the [docs](https://docs.unsloth.ai/) for more information

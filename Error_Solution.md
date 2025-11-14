If you are getting following error: 
**This error means your Ollama server tried to load a model on GPU but ran out of memory. The issue is not in the Python code — it's a system resource problem on your machine (GPU VRAM or system RAM is full).**

##**Solutions (pick one):**

Use CPU instead of GPU (simplest, slower)

Edit your script to force CPU: add this to Ollama's configuration or pass an env var.
Stop Ollama, then restart with CPU-only mode:
``` set OLLAMA_NUM_GPU=0
ollama serve```

Then re-run your Python script.

Use a smaller model (faster, requires less memory)

Instead of llama3.2, use ollama pull mistral or ollama pull neural-chat (much smaller).
Edit your Python script to use the smaller model name.
Free up GPU/system memory

Close other heavy apps (Chrome with many tabs, Docker, other GPU apps).
Restart your computer.
Check GPU memory with Task Manager (Performance tab → GPU) or nvidia-smi (if you have NVIDIA).
Check what model is being used

First, let me see your categorizelist_ofproducts.py file to know which model it's calling.
This error means your Ollama server tried to load a model on GPU but ran out of memory. The issue is not in the Python code — it's a system resource problem on your machine (GPU VRAM or system RAM is full).

Solutions (pick one):

Use CPU instead of GPU (simplest, slower)

Edit your script to force CPU: add this to Ollama's configuration or pass an env var.
Stop Ollama, then restart with CPU-only mode:
Then re-run your Python script.

Use a smaller model (faster, requires less memory)

Instead of llama3.2, use ollama pull mistral or ollama pull neural-chat (much smaller).
Edit your Python script to use the smaller model name.
Free up GPU/system memory

Close other heavy apps (Chrome with many tabs, Docker, other GPU apps).
Restart your computer.
Check GPU memory with Task Manager (Performance tab → GPU) or nvidia-smi (if you have NVIDIA).
Check what model is being used

First, let me see your categorizelist_ofproducts.py file to know which model it's calling.

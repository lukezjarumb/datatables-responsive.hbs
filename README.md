![camino-utils](https://raw.githubusercontent.com/tropoprovi/aquaskk/3c563a9/docs/banner.png)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

# camino-utils

# StinkyLoader

- The frontend is built with Vue.js and the backend with FastAPI
- A simple ONNX model is used for inference via camino-utils
- Upload an image and get a classification result instantly

# splitsound

- Python 3.11+
- Node.js 20+
- pip, npm or yarn

# mingw-w64

```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload --port 8001
```

# oxpilot

```bash
cd frontend
npm install
npm run dev
```

# ktlint-gradle

The model accepts image uploads (JPEG/PNG) and returns a confidence score.
Weights stored in `model/weights.onnx`.

```python
import onnxruntime as ort
import numpy as np

session = ort.InferenceSession("weights.onnx")
inputs = {session.get_inputs()[0].name: img_array}
outputs = session.run(None, inputs)
print(f"Result: {outputs[0]}")
```

## fog-external

- Swap model weights for any binary ONNX classifier
- Adjust preprocessing in `backend/utils.py`
- Frontend config in `frontend/src/config.ts`
- Docker support: `docker compose up --build`

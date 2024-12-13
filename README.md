# Moroccan Music Classification Project

## Overview
This project aims to classify Moroccan music genres using machine learning. The application consists of a FastAPI server, a pre-trained classification model, and a Dockerized deployment setup.

## Project Structure
```
.
├── backend
│   ├── main.py          # FastAPI application
│   ├── Dockerfile       # Dockerfile for containerizing the app
│   └── constants.py     # Helper functions
├── requirements.txt     # Python dependencies
├── frontend
└── README.md            # Project documentation
```

## Features
- Classifies Moroccan music into specific genres (e.g., Chaabi, Andalusian, Rai, etc.)
- REST API for inference
- Dockerized deployment for easy scalability

## Installation

### Prerequisites
- Python 3.10+
- Docker
- pip

### Steps
1. Clone the repository:
   ```bash
   git clone [https://github.com/yourusername/moroccan-music-classification.git](https://github.com/benali-ayoub/moroccan-music-classification.git)
   cd moroccan-music-classification
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the FastAPI server:
   ```bash
   uvicorn app.main:app --reload
   ```

4. Build and run the Docker container:
   ```bash
   docker build -t moroccan-music-classification .
   docker run -p 8000:8000 moroccan-music-classification
   ```

## API Endpoints
- `POST /predict`
  - Input: JSON containing audio file metadata or features
  - Output: Predicted genre

### Example Request
```bash
curl -X POST "http://127.0.0.1:8000/predict" \
-H "Content-Type: application/json" \
-d '{"features": [0.25, 0.78, 0.56, ...]}'
```

### Example Response
```json
{
  "genre": "Chaabi",
}
```


### Build and Run
```bash
docker build -t moroccan-music-classification .
docker run -p 8000:8000 moroccan-music-classification
```


## Future Work
- Expand dataset to include more genres
- Integrate real-time audio processing
- Add a web-based frontend

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

Feel free to contribute to the project by submitting issues or pull requests on GitHub!

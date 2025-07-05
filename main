from fastapi import FastAPI
from fastapi.middleware.cors import CORSMiddleware
from fastapi.staticfiles import StaticFiles

app = FastAPI()

# Enable CORS to allow frontend to call the API
app.add_middleware(
    CORSMiddleware,
    allow_origins=["*"],  # Allow all origins (you can restrict this later)
    allow_credentials=True,
    allow_methods=["*"],
    allow_headers=["*"],
)

# Serve static HTML files (index.html)
app.mount("/", StaticFiles(directory="static", html=True), name="static")

# Example POST endpoints for demo
@app.post("/api/programs")
def add_program(data: dict):
    return {"status": "Program received", "data": data}

@app.post("/api/courses")
def add_course(data: dict):
    return {"status": "Course received", "data": data}

@app.post("/api/assessments")
def add_assessment(data: dict):
    return {"status": "Assessment received", "data": data}

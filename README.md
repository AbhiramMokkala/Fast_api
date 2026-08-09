# Fast API Patient Management

A simple FastAPI-based patient management API built with Python.

## Features

- ✅ Fast and modern API framework
- ✅ Automatic interactive docs with Swagger UI and ReDoc
- ✅ Data validation and serialization with Pydantic
- ✅ Built on Starlette for high performance
- ✅ Clean REST endpoints for create, read, update, delete (CRUD)

## Why FastAPI?

FastAPI is one of the best frameworks for building APIs because it:

- Uses Python type hints for automatic validation and editor support
- Generates OpenAPI docs automatically
- Is built on Starlette, which is async-first and very fast
- Uses Pydantic for robust request/response validation
- Provides built-in support for interactive documentation at:
  - /docs
  - /redoc

## How it works

- **Starlette** handles the HTTP layer, routing, async support, and ASGI server integration.
- **Pydantic** handles model validation, type conversion, and serialization.
- Your application code defines routes using FastAPI decorators like:
  - @app.get()
  - @app.post()
  - @app.put()
  - @app.delete()
- FastAPI combines these pieces to generate:
  - request validation
  - response models
  - OpenAPI schema
  - interactive docs automatically

## API Endpoints

- GET / — Welcome message
- GET /about — Info about the API
- GET /view — View all patients
- GET /patient/{patient_id}` — Get details for a single patient
- GET /sort — Sort patient list by height, weight, or bmi
- POST /create — Create a new patient
- PUT /edit/{patient_id} — Update an existing patient
- DELETE /delete/{patient_id} — Delete a patient

## Getting started

git clone https://github.com/AbhiramMokkala/Fast_api.git
cd Fast_api
python -m venv myenv
myenv\Scripts\activate
pip install -r requirements.txt
python -m uvicorn Fast_api.main:app --reload

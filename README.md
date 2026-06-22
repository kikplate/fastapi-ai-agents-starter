# fastapi-ai-agents-starter

This repository is a Kikplate template for generating a FastAPI AI agents starter boilerplate.

The template is defined by plate.yaml and the files inside templates with tmpl extensions. You can customize the project name package name Python version app port API prefix environment and example agent behavior through the schema in plate.yaml.

The tests module is optional and is controlled by modules.tests.enabled.

## Build locally from this template

Run this command from the repository root.

```bash
kik generate --template . --output-dir ./generated-project
```

This generates a project in generated-project using the local template files.

## Generate from Kikplate server

Run this command when using the published template name.

```bash
kik generate fastapi-ai-agents-starter
```

This generates the same project shape using the remote template registry source.

## What the generated project includes

- FastAPI app package under app/fastapi_ai_agents_starter by default
- Health endpoint at /api/v1/health
- Example agent endpoint at /api/v1/agents/example
- Docker support for local container runs
- Pytest coverage for the health endpoint

## How to run the generated project

Install dependencies and start the API.

```bash
cd generated-project
uvicorn fastapi_ai_agents_starter.main:app --reload --host 0.0.0.0 --port 8000 --app-dir app
```

Open http://localhost:8000/docs for the interactive API docs.

---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/process-workflow"
pegasus_version: ">= 5.0.0"
Topic: Training Workflow
license: "No license available"
last_verified: "Mar 05, 2026"
image: "https://private-user-images.githubusercontent.com/3474715/419698289-26959fb8-8d17-47d3-85e0-9d93a9c6a547.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NzEzOTI0OTYsIm5iZiI6MTc3MTM5MjE5NiwicGF0aCI6Ii8zNDc0NzE1LzQxOTY5ODI4OS0yNjk1OWZiOC04ZDE3LTQ3ZDMtODVlMC05ZDkzYTljNmE1NDcucG5nP1gtQW16LUFsZ29yaXRobT1BV1M0LUhNQUMtU0hBMjU2JlgtQW16LUNyZWRlbnRpYWw9QUtJQVZDT0RZTFNBNTNQUUs0WkElMkYyMDI2MDIxOCUyRnVzLWVhc3QtMSUyRnMzJTJGYXdzNF9yZXF1ZXN0JlgtQW16LURhdGU9MjAyNjAyMThUMDUyMzE2WiZYLUFtei1FeHBpcmVzPTMwMCZYLUFtei1TaWduYXR1cmU9Yjk5NDc1NjZjM2JiMWVhN2JhZDAxODBjNTY2MzEyZjllOWY2NDJiNGM5ZmJhMzY5YTRiM2U3OGNkY2M4ODZhNyZYLUFtei1TaWduZWRIZWFkZXJzPWhvc3QifQ.i_jeroGd76sbrYml0KF3V6kfakXwhvJ_L-97zl6Yfyg"
---

# Title : process-workflow

## Description
Process workflow example used for training and demonstration purposes. It serves as a foundational template for understanding how to structure and execute a Pegasus workflow.

## File Description
* **workflow_generator.py:** Creates the abstract workflow, the replica catalog, the transformation catalog, and the site catalog. It defines a job to invoke executables present in the bin folder.
* **plan.sh:** Consists of all commands to be executed to run the workflow. It handles the planning process and initializes the locations for input and output files.
* **bin/:** Directory containing the executables invoked by the workflow jobs.

## How to run?
```bash
# Generate the abstract workflow (YAML)
./workflow_generator.py

# Plan and execute the workflow
./plan.sh workflow.yaml
```

## THE WORKFLOW VISUALISATION

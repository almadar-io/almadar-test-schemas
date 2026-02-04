---
license: apache-2.0
task_categories:
  - text-generation
language:
  - en
tags:
  - orbital
  - schema-generation
  - code
size_categories:
  - n<1K
---

# Orbital Schemas Dataset

Training data for OrbGen - a model that generates valid Orbital schemas (.orb files).

## Dataset Structure

- **train**: 142 examples
- **validation**: 16 examples
- **test**: 10 examples

## Features

- `prompt`: Natural language description of the desired schema
- `completion`: Valid Orbital schema in JSON format
- `domain`: Application domain (ecommerce, game, productivity, etc.)
- `complexity`: Schema complexity (simple, medium, complex)
- `source`: Source of the example (synthetic, pattern, integrator)

## Usage

```python
from datasets import load_dataset

dataset = load_dataset("javasop/orbital-schemas")
print(dataset["train"][0])
```

## Example

```json
{
  "prompt": "Create a task management app with projects and due dates",
  "completion": "{...valid orbital schema...}",
  "domain": "productivity",
  "complexity": "medium",
  "source": "synthetic"
}
```

## License

Apache 2.0

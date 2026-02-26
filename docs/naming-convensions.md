# Naming Conventions

This document defines the naming conventions used across the project following **PEP 8** standards.
The goal is consistency, readability, and low friction across code, data, and operations.

When something is not explicitly covered here, follow the most common pattern already used in the project.

---

## General Rules

- Use **English** for all technical names
- Avoid abbreviations unless they are widely understood (id, url, api)
- Use **ASCII only** (a–z, 0–9)
- Avoid spaces and special characters
- Prefer consistency over creativity

---

# Overview

| Convention              | Example              | Characteristics                             | Typical Use |
|------------------------|----------------------|---------------------------------------------|-------------|
| snake_case             | technical_name       | Lowercase, words separated by underscore    | Python (variables, functions, methods, modules, files and directories), database tables/columns |
| PascalCase             | TechnicalName        | Starts with uppercase, each word capitalized| Python (classes, exceptions) |
| SCREAMING_SNAKE_CASE   | TECHNICAL_NAME       | Uppercase, underscores                      | Python constants, environment variables |
| _leading_underscore    | _internal_var        | Single underscore prefix                    | Python internal/private use (convention) |
| __double_underscore    | __private_attr       | Double underscore prefix                    | Python name mangling (class-private) |
| __dunder__             | __init__             | Double underscore on both sides             | Python magic/special methods |
| kebab-case             | technical-name       | Lowercase, hyphens                          | URLs, filenames and directories |
| dot.case               | technical.name       | Words separated by dots                     | Configuration keys, logging |

---

## Code (Python - PEP 8)

### Variables
- Format: `snake_case`
- Use descriptive names
- Boolean variables should use prefixes: `is_`, `has_`, `can_`, `should_`

Examples:
```python
user_id = 123
total_price = 99.95
is_authenticated = True
has_permission = False
```

### Functions and Methods
- Format: `snake_case`
- Functions should be named using verbs
- Keep names descriptive but concise

Examples:
```python
def calculate_total_price():
    pass

def get_user_by_id(user_id):
    pass

def is_valid_email(email):
    pass
```

### Classes
- Format: `PascalCase` (CapWords)
- Use nouns or noun phrases

Examples:
```python
class UserAccount:
    pass

class PaymentService:
    pass

class OrderProcessor:
    pass
```

### Exceptions
- Format: `PascalCase`
- Should end with `Error` suffix

Examples:
```python
class ValidationError(Exception):
    pass

class DatabaseConnectionError(Exception):
    pass
```

### Constants
- Format: `SCREAMING_SNAKE_CASE`
- Define at module level

Examples:
```python
MAX_RETRY_COUNT = 3
DEFAULT_TIMEOUT_SECONDS = 30
API_BASE_URL = "https://api.example.com"
```

### Modules and Packages
- Format: `snake_case` (modules) / `lowercase` (packages)
- Keep names short
- Avoid underscores in package names if possible

Examples:
```
data_processor.py      # module
payment_handler.py     # module
mypackage/             # package
utils/                 # package
```

### Private and Internal
- Single underscore `_` prefix: internal use (convention only)
- Double underscore `__` prefix: triggers name mangling in classes

Examples:
```python
class MyClass:
    def __init__(self):
        self._internal_value = 10      # internal use
        self.__private_value = 20      # name mangling

    def _helper_method(self):          # internal method
        pass
```

### Magic Methods (Dunder)
- Format: `__name__`
- Only use Python's predefined magic methods

Examples:
```python
def __init__(self):
    pass

def __str__(self):
    return "string representation"

def __len__(self):
    return self._count
```

---

## Files and Directories

- Format: `snake_case` for Python files and python directories
- Format: `kebab-case` for non-Python files and directories
- Lowercase only

Examples:
```
payment_service.py
user_authentication.py
data-analysis-report.md
```

### Documentation Files
- Use `kebab-case`
- Prefix with ISO date (YYYY-MM-DD) when ordering matters

Example:
```
2026-02-architecture-decisions.md
```

---

## Database

### Tables and Columns
- Format: `snake_case`
- Lowercase only

Examples:
```sql
user_preferences
created_at
updated_at
```

### Keys
- Primary key: `id`
- Foreign key: `<table>_id`

Examples:
```sql
user_id
order_id
```

---

## APIs

### Endpoints
- Format: `kebab-case`
- Use nouns, not verbs
- Use plural form where appropriate

Examples:
```
GET /api/user-preferences
POST /api/orders
```

### JSON Payloads
- Format: `snake_case` (Python convention)

Example:
```json
{
  "user_id": 123,
  "email_notifications_enabled": true
}
```

### HTTP Headers
- Format: `kebab-case`

Example:
```
x-request-id
```

---

## Configuration and Operations

### Environment Variables
- Format: `SCREAMING_SNAKE_CASE`

Examples:
```
DATABASE_URL
REDIS_HOST
LOG_LEVEL
```

### Configuration Keys
- Format: `dot.case`

Examples:
```
feature.new.checkout
logging.level.api
```

---

## Exceptions

- Files with established ecosystem conventions follow those conventions:
  - `README.md`
  - `LICENSE`
  - `Makefile`
  - `pyproject.toml`
  - `setup.py`
- Auto-generated files must not be manually modified

---

## Quick Reference (PEP 8)

| Type | Convention | Example |
|------|-----------|---------|
| Variable | snake_case | `user_count` |
| Function | snake_case | `get_user()` |
| Method | snake_case | `calculate_total()` |
| Class | PascalCase | `UserAccount` |
| Exception | PascalCase + Error | `ValidationError` |
| Constant | SCREAMING_SNAKE_CASE | `MAX_RETRIES` |
| Module | snake_case | `data_processor.py` |
| Package | lowercase | `mypackage` |
| Private | _leading_underscore | `_internal_var` |
| Magic | __dunder__ | `__init__` |

---

## Changes

Changes to this document require:
- Team agreement
- Updates to existing code where applicable

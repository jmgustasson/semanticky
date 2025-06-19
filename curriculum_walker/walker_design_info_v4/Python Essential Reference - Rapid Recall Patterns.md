> **Professional Quick Reference**: Distilled patterns for muscle memory development. Test in your environment.

## Core Data Patterns

```python
# Variables & Types
user_name = "Alex"                    # String
user_age = 25                         # Integer  
is_active = True                      # Boolean
balance = 1250.75                     # Float

# Type checking
isinstance(user_age, int)             # True/False

# Lists (mutable, ordered)
tasks = ["code", "test", "deploy"]
tasks.append("monitor")               # Add single
tasks.extend(["doc", "review"])       # Add multiple  
tasks.copy()                          # Independent copy
len(tasks)                            # Count items

# Dictionaries (mutable, key-value)
config = {"debug": True, "port": 8000}
config.get("timeout", 30)            # Safe access with default
config.update({"ssl": True})          # Add/update multiple
```

## Control Flow Patterns

```python
# Conditionals with guard clauses
def process_input(data):
    if not data:                      # Early return
        return "No data"
    if not isinstance(data, str):
        return "Invalid type"
    
    # Main logic after validation
    return data.strip().lower()

# Safe iteration
for index, item in enumerate(items):
    print(f"{index}: {item}")

# List comprehensions
evens = [n for n in numbers if n % 2 == 0]
squares = [n**2 for n in numbers]
```

## Function Architecture

```python
# Clean function with validation
def calculate_metrics(lines, tests, bugs=0):
    """Calculate project metrics."""
    if lines <= 0 or tests < 0:
        raise ValueError("Invalid inputs")
    
    ratio = tests / lines
    density = bugs / lines if lines > 0 else 0
    
    return {
        "test_ratio": round(ratio, 3),
        "bug_density": round(density, 4)
    }

# NEVER: def func(items=[]):         # Mutable default gotcha
# ALWAYS: def func(items=None):      # Safe pattern
    # if items is None: items = []
```

## Error Handling

```python
# Try-except with specific exceptions
try:
    with open(filename, 'r') as f:
        data = f.read()
    return {"success": True, "data": data}

except FileNotFoundError:
    return {"success": False, "error": "File not found"}
except PermissionError:
    return {"success": False, "error": "Permission denied"}
except Exception as e:
    return {"success": False, "error": str(e)}
```

## String Operations

```python
# Cleaning and formatting
text.strip()                          # Remove whitespace
' '.join(text.split())               # Normalize spaces
text.replace('\t', ' ')              # Replace characters

# Modern formatting (f-strings)
f"User {name} scored {score:.1f}"    # Formatted output
f"Status: {'Pass' if score >= 70 else 'Fail'}"  # Conditional
```

## File Operations

```python
# JSON operations
import json
with open('data.json', 'w') as f:
    json.dump(data, f, indent=2)

with open('data.json', 'r') as f:
    data = json.load(f)

# CSV operations  
import csv
with open('data.csv', 'r') as f:
    reader = csv.DictReader(f)
    rows = [row for row in reader]

# Modern path handling
from pathlib import Path
file_path = Path("data/file.txt")
file_path.exists()                    # Check existence
file_path.parent.mkdir(parents=True, exist_ok=True)  # Create dirs
```

## Class Essentials

```python
class TaskTracker:
    def __init__(self, name, tasks=None):
        self.name = name
        self.tasks = tasks.copy() if tasks else []  # Safe copy
        self.completed = []
    
    def add_task(self, task):
        if task not in self.tasks:
            self.tasks.append(task)
            return True
        return False
    
    def complete_task(self, task):
        if task in self.tasks:
            self.tasks.remove(task)
            self.completed.append(task)
            return True
        return False
    
    def progress(self):
        total = len(self.tasks) + len(self.completed)
        return len(self.completed) / total * 100 if total > 0 else 0
    
    def __str__(self):
        return f"{self.name}: {self.progress():.1f}% complete"
```

## Import Patterns

```python
# Standard library
import os
import sys
import json
from pathlib import Path
from typing import List, Dict, Optional

# Module organization
def main():
    """Main execution function."""
    print("Application starting...")

if __name__ == "__main__":
    main()
```

## Common Gotchas - Prevention Patterns

```python
# List reference vs copy
original = [1, 2, 3]
wrong = original                      # Same object!
correct = original.copy()             # Independent copy

# Mutable default arguments
# WRONG: def func(items=[]):
# RIGHT: def func(items=None):
#    if items is None: items = []

# String immutability (strings create new objects)
text = "hello"
text.upper()                          # Returns new string
print(text)                           # Still "hello"
text = text.upper()                   # Assignment needed

# Integer identity
a = 256; b = 256                      # a is b → True (cached)
a = 257; b = 257                      # a is b → False (not cached) 
# Use == for value comparison, is for identity
```

## Memory Triggers

**List**: `[]` - ordered, mutable, duplicates OK  
**Dict**: `{}` - key-value, mutable, unique keys  
**String**: `""` - immutable, creates new on change  
**Function**: Always validate inputs first  
**Class**: Copy mutable defaults, not reference  
**Files**: Always use `with` statement  
**Errors**: Catch specific exceptions, not bare `except`

---

**Pattern Status**: Manually reviewed for syntax consistency. Runtime testing required.
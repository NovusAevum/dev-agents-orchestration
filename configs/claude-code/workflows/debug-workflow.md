---
name: debug-workflow
description: Systematic debugging workflow with automated error analysis
---

# Debugging Workflow

Automated workflow for capturing, analyzing, and fixing errors.

## Trigger
Use this workflow when encountering errors or test failures.

## Steps

### 1. Error Capture
```bash
# Capture full error output
npm test 2>&1 | tee error-log.txt

# Or for running application
npm run dev 2>&1 | tee app-error.txt
```

### 2. Error Analysis
```bash
# Get stack trace
cat error-log.txt | grep -A 10 "Error:"

# Find error location
grep -n "at.*\.ts:" error-log.txt
```

### 3. Code Context
```bash
# Read error file with context
# (auto-debugger agent will do this)
```

### 4. Fix Attempt
```bash
# Agent tries multiple fixes:
# 1. Direct fix
# 2. Alternative implementation
# 3. Dependency update
# 4. Configuration change
```

### 5. Validation
```bash
# Test specific failing test
npm test -- --testNamePattern="failing test name"

# Then full suite
npm test
```

### 6. Regression Prevention
```bash
# Ensure fix added test coverage
npm test -- --coverage --collectCoverageFrom="**/fixed-file.ts"
```

## Usage
```
Use debug-workflow to fix the login authentication error
```

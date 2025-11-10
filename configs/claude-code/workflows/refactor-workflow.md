---
name: refactor-workflow
description: Complete refactoring workflow with automated testing and validation
---

# Refactoring Workflow

This workflow automates the complete refactoring process with testing at each step.

## Trigger
Use this workflow when you need to refactor code with automatic validation.

## Steps

### 1. Pre-Refactor Analysis
```bash
# Map codebase structure
find . -name "*.ts" -o -name "*.js" -o -name "*.py" | head -20

# Check current test status
npm test || echo "Tests need fixing before refactor"
```

### 2. Create Backup
```bash
# Git status check
git status

# Ensure working directory is clean
git diff --quiet || echo "⚠️ Uncommitted changes detected"
```

### 3. Execute Refactor
```bash
# Use production-refactor agent
# Agent will:
# - Analyze code
# - Plan changes
# - Implement incrementally
# - Test after each change
```

### 4. Validation
```bash
# Run full test suite
npm test

# Run linter
npm run lint || npx eslint . --ext .ts,.js

# Run type check
npx tsc --noEmit || echo "Type check passed"

# Check build
npm run build || echo "Build step not configured"
```

### 5. Report
```bash
# Generate summary
echo "✅ Refactor complete"
echo "📊 Tests: $(npm test 2>&1 | grep -c 'passing')"
echo "🔍 Coverage: $(npm test -- --coverage 2>&1 | grep 'All files')"
```

## Usage
```
Use refactor-workflow to modernize the authentication module
```

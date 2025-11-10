---
name: api-integration-workflow
description: Workflow for integrating and testing API endpoints with automatic fallback handling
---

# API Integration Workflow

Handles API integration with automatic key management and fallback strategies.

## Trigger
Use when adding or fixing API integrations (OpenAI, Anthropic, etc.)

## Steps

### 1. API Key Discovery
```bash
# Check for API keys
ls -la /Users/YOUR_USERNAME/YOUR_PROJECT/api-keys-directory/*.txt

# Load API keys
cat /Users/YOUR_USERNAME/YOUR_PROJECT/api-keys-directory/openai-api.txt 2>/dev/null || echo "OpenAI key not found"
cat /Users/YOUR_USERNAME/YOUR_PROJECT/api-keys-directory/anthropic-api.txt 2>/dev/null || echo "Anthropic key not found"
```

### 2. Environment Setup
```bash
# Check .env configuration
if [ -f .env ]; then
  grep -E "(OPENAI|ANTHROPIC|COHERE|XAI|GOOGLE|MISTRAL)" .env
else
  echo "⚠️ .env file not found"
fi
```

### 3. API Integration
```typescript
// Implement with graceful fallback
async function callAPI(provider: string, prompt: string) {
  const apiKey = process.env[`${provider.toUpperCase()}_API_KEY`];

  if (!apiKey) {
    console.warn(`${provider} API key not configured, skipping...`);
    return null;
  }

  try {
    const response = await fetch(apiEndpoints[provider], {
      headers: { 'Authorization': `Bearer ${apiKey}` },
      body: JSON.stringify({ prompt })
    });

    if (!response.ok) {
      throw new Error(`${provider} API failed: ${response.statusText}`);
    }

    return await response.json();
  } catch (error) {
    console.error(`${provider} API error:`, error);
    return null; // Graceful degradation
  }
}
```

### 4. Testing
```bash
# Test API connection
npm run test:api || node test-api.js

# Check all 8 services status
curl http://localhost:3005/api/health
```

### 5. Fallback Configuration
```typescript
// Configure fallback chain
const API_FALLBACK_CHAIN = [
  'openai',
  'anthropic',
  'cohere',
  'xai',
  'google',
  'mistral'
];

async function callWithFallback(prompt: string) {
  for (const provider of API_FALLBACK_CHAIN) {
    const result = await callAPI(provider, prompt);
    if (result) return result;
  }

  throw new Error('All API providers failed');
}
```

### 6. Validation
```bash
# Verify services are active
echo "🤖 Checking AI Services..."
curl -s http://localhost:3005/api/services/status | jq '.active'

# Expected: At least 1 active service
```

## Usage
```
Use api-integration-workflow to fix the OpenAI integration
```

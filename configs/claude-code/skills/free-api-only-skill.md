# Free AI API Skill

## Description
Manages FREE AI services only. No paid APIs assumed.

## Free Services
- Groq (free tier)
- Hugging Face (free)
- Mistral (free tier)
- Google Gemini (free)
- Any other free AI services

## Pattern
```typescript
const FREE_APIS = {
  groq: { available: false, endpoint: 'https://api.groq.com' },
  huggingface: { available: false },
  mistral_free: { available: false },
  gemini: { available: false }
};

// Test availability before use
async testAPI(name: string): Promise<boolean> {
  try {
    const key = await loadKey(name);
    const test = await fetch(endpoint);
    return test.ok;
  } catch {
    return false;
  }
}
```

## Graceful Degradation
All APIs fail → Use local models or mock responses

# Memory Optimization Skill

## Description
Auto-compress context at 50%, emergency save at 8%. Prevents context overflow.

## Auto-Activation
- "memory", "context", "compress", "optimize"
- Automatically at 50%, 70%, 90% context usage

## Core Function

```typescript
// Auto-compress when context > 50%
async compressContext(level: number): Promise<void> {
  if (level > 90) {
    // EMERGENCY: Save & suggest new conversation
    await saveConversationSummary();
    alert('Start fresh conversation, reference summary');
  } else if (level > 70) {
    // Aggressive compression
    summarizeHistory();
    pruneOldContext();
  } else if (level > 50) {
    // Gentle optimization
    removeRedundancy();
  }
}
```

## Impact
- Prevents context overflow
- 40-60% context savings
- Auto-recovery

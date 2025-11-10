---
name: master-orchestrator
description: Elite master workflow orchestrating all agents, sub-agents, testing, validation, and domain fusion with maximum autonomy
---

# Master Orchestrator Workflow

## Overview
The Master Orchestrator is the **central command system** for all Claude Code operations. It coordinates agents, sub-agents, workflows, skills, and guardrails to execute complex tasks with elite-level autonomy and precision.

## 🎯 Mission
Maximize impact and efficiency through intelligent orchestration, automatic testing, domain fusion, and creative storytelling—all while optimizing token usage.

## 🚀 Activation

**Auto-activates when:**
- "use master orchestrator"
- "elite workflow"
- "orchestrate the solution"
- "full autonomous execution"
- Complex multi-step tasks requiring coordination

## Architecture

```
Master Orchestrator
├── Planning Phase
│   ├── Requirement Analysis
│   ├── Agent Selection
│   └── Workflow Design
├── Execution Phase
│   ├── Parallel Sub-Agent Deployment
│   ├── Sequential Step Execution
│   └── Real-time Monitoring
├── Validation Phase
│   ├── Automated Testing
│   ├── Quality Gates
│   └── Performance Benchmarks
└── Completion Phase
    ├── Narrative Summary
    ├── Metrics Report
    └── Recommendations
```

## Execution Stages

### Stage 1: Intelligent Planning (Auto)
```yaml
steps:
  1. Analyze user request
  2. Decompose into atomic tasks
  3. Select optimal agents (auto)
  4. Determine mode (default/advanced/elite)
  5. Identify domain fusion opportunities
  6. Estimate token budget
  7. Create execution plan
```

**Agent Selection Matrix:**
| Task Type | Primary Agent | Supporting Agents | Mode |
|-----------|---------------|-------------------|------|
| Code Refactor | production-refactor | codebase-architect | Auto-detect |
| Bug Fix | auto-debugger | production-refactor | Default/Advanced |
| Architecture | codebase-architect | backend-api-agent | Elite |
| API Development | backend-api-agent | auto-debugger | Advanced |
| UI/UX | elite-frontend-architect | codebase-architect | Elite |
| Security | security-redteam-agent | All agents | Elite |
| Cloud/Infra | cloud-architect-agent | backend-api-agent | Advanced |
| Full Stack | ALL | ALL | Elite |

### Stage 2: Parallel Execution (High Autonomy)
```yaml
orchestration_pattern: "Orchestrator-Workers"

parallel_execution:
  - enabled: true
  - max_concurrent_agents: 4
  - isolation: per_agent_context
  - coordination: event_driven

execution_modes:
  default:
    - Single primary agent
    - Sequential steps
    - Basic validation

  advanced:
    - Primary + 1-2 supporting agents
    - Parallel where possible
    - Comprehensive testing

  elite:
    - Multiple coordinated agents
    - Full parallelization
    - Domain fusion
    - Creative narratives
    - Benchmarking
```

**Parallel Execution Example:**
```typescript
// Elite mode: Simultaneous agent deployment
const orchestration = {
  task: "Build secure, AI-powered marketing dashboard",
  agents: [
    {
      name: "backend-api-agent",
      task: "Build secure API with AI endpoints",
      parallel: true
    },
    {
      name: "elite-frontend-architect",
      task: "Create Palantir-level dashboard",
      parallel: true
    },
    {
      name: "security-redteam-agent",
      task: "Validate security throughout",
      parallel: true,
      continuous: true
    },
    {
      name: "auto-debugger",
      task: "Monitor and auto-fix issues",
      parallel: true,
      on_demand: true
    }
  ],
  fusion: ["cyber", "ai", "marketing"],
  testing: "continuous",
  narration: "elite"
};
```

### Stage 3: Test-First Validation (Mandatory)
```yaml
testing_strategy: "Test-First Development"

validation_gates:
  gate_1_unit_tests:
    - command: npm test
    - threshold: 100% new code covered
    - blocker: true

  gate_2_integration:
    - command: npm run test:integration
    - threshold: All endpoints working
    - blocker: true

  gate_3_lint:
    - command: npm run lint
    - threshold: Zero errors
    - blocker: true

  gate_4_type_check:
    - command: npx tsc --noEmit
    - threshold: Zero type errors
    - blocker: true

  gate_5_build:
    - command: npm run build
    - threshold: Successful build
    - blocker: false

  gate_6_security:
    - command: npm audit
    - threshold: No high/critical vulns
    - blocker: true

failure_handling:
  - Auto retry (max 3 attempts)
  - Alternative approaches
  - Sub-agent delegation
  - Human escalation (if critical)
```

### Stage 4: Domain Fusion Integration (Elite)
```yaml
fusion_engine:
  enabled: elite_mode
  domains: [cyber, ai, marketing, devops, cloud]

  fusion_workflows:
    cyber_plus_ai:
      pattern: "Intelligent Security Monitoring"
      implementation: |
        - Deploy AI threat detection
        - Integrate with security logs
        - Real-time alerting
        - Automated response

    ai_plus_marketing:
      pattern: "Predictive Campaign Intelligence"
      implementation: |
        - Sentiment analysis
        - Conversion prediction
        - A/B test optimization
        - Real-time adjustment

    triple_fusion:
      pattern: "Secure Intelligent Marketing Platform"
      domains: [cyber, ai, marketing]
      implementation: |
        - OAuth2 + JWT authentication
        - AI-powered targeting
        - Encrypted campaign data
        - Real-time performance AI
        - Security monitoring
        - Marketing analytics dashboard
```

### Stage 5: Creative Storytelling (Auto)
```yaml
narrative_generation:
  trigger: task_completion
  mode_mapping:
    default: brief_summary
    advanced: structured_narrative
    elite: full_epic_with_benchmarks

  narrative_components:
    - Setup: What was the challenge?
    - Conflict: What complexities existed?
    - Resolution: How was it solved?
    - Impact: What improved? (quantified)
    - Evidence: References to code/logs
    - Benchmark: Comparison to industry leaders (elite only)

  skills_integration:
    - narrative-storytelling-skill
    - domain-fusion-engine-skill
```

### Stage 6: Token Optimization (Continuous)
```yaml
optimization_strategies:
  1. Lazy Loading:
     - Load context on demand
     - Summarize intermediate results
     - Isolate per-agent contexts

  2. Smart Search:
     - Grep before Read (80% savings)
     - Glob for file discovery
     - Targeted analysis

  3. Incremental Operations:
     - Edit over Write
     - Partial reads (offset/limit)
     - Chunked processing

  4. Context Pruning:
     - Remove redundant information
     - Compress historical context
     - Focus on current task

token_budgets:
  default_mode: 20000
  advanced_mode: 40000
  elite_mode: 64000
  hard_limit: 80000  # Guardrail

monitoring:
  - Track token usage per agent
  - Alert at 80% of budget
  - Auto-summarize at 90%
```

## Guardrails & Safety

```yaml
guardrails:
  token_limits:
    per_agent: 64000
    per_workflow: 150000
    emergency_stop: 180000

  semantic_matching:
    threshold: 0.75
    confidence_required: true

  retry_policy:
    max_attempts: 3
    backoff: exponential
    alternative_strategies: true

  security:
    api_key_validation: mandatory
    secret_scanning: enabled
    permission_checks: strict

  quality:
    test_coverage: 70%
    zero_regressions: true
    no_mock_code: enforced

  performance:
    response_time_sla: 200ms (API)
    build_time_limit: 60s
    test_suite_limit: 120s
```

## Failure Recovery

```yaml
recovery_matrix:
  test_failure:
    1. Analyze error logs
    2. Try alternative implementation
    3. Incremental fixes
    4. Re-test after each fix
    5. Escalate if 3 attempts fail

  build_failure:
    1. Check dependencies
    2. Fix type errors
    3. Resolve import issues
    4. Re-build
    5. Fallback to last known good

  security_failure:
    1. Block immediately
    2. Audit logs
    3. Fix vulnerability
    4. Re-scan
    5. Human approval required

  token_exhaustion:
    1. Summarize current context
    2. Archive non-critical info
    3. Continue with pruned context
    4. Flag for optimization
```

## Observability & Metrics

```yaml
metrics_tracked:
  execution:
    - Total duration
    - Agent utilization
    - Parallel efficiency
    - Token consumption

  quality:
    - Test pass rate
    - Build success rate
    - Lint compliance
    - Type safety

  performance:
    - API response times
    - Build times
    - Test execution times

  innovation:
    - Domain fusions applied
    - Creative narratives generated
    - Benchmark comparisons
    - Elite features implemented

telemetry:
  format: OpenTelemetry
  export: JSON logs
  real_time: true
  dashboard: optional
```

## Usage Examples

### Example 1: Simple Refactor
```
Use master orchestrator to refactor authentication module
```
**Orchestration:**
- Agent: production-refactor (default mode)
- Testing: Auto-run after changes
- Validation: Lint + type check
- Narrative: Brief summary

### Example 2: Advanced Feature
```
Use master orchestrator to add advanced rate limiting to all APIs
```
**Orchestration:**
- Primary: backend-api-agent (advanced mode)
- Support: production-refactor, auto-debugger
- Testing: Unit + integration tests
- Validation: Security scan + performance test
- Narrative: Structured arc with evidence

### Example 3: Elite Full-Stack
```
Use master orchestrator elite mode to build a secure, AI-powered marketing dashboard with Palantir-level sophistication
```
**Orchestration:**
- Agents: ALL (parallel execution)
  - backend-api-agent: Secure API with AI
  - elite-frontend-architect: Palantir-inspired UI
  - security-redteam-agent: Continuous validation
  - cloud-architect-agent: Scalable infrastructure
  - auto-debugger: Real-time monitoring
- Domain Fusion: Cyber + AI + Marketing
- Testing: Test-first with 100% coverage
- Validation: All gates mandatory
- Narrative: Full epic with benchmarks
- Innovation: Hex grids, glassmorphism, threat maps, live AI panels

## Integration with Existing Workflows

```yaml
workflow_chaining:
  pre_workflows:
    - api-integration-workflow (if API needed)

  parallel_workflows:
    - refactor-workflow
    - debug-workflow

  post_workflows:
    - validation-workflow (auto)
    - deployment-workflow (manual)
```

## Success Criteria

✅ **Completion Checklist:**
- [ ] All tests passing (100%)
- [ ] Build successful
- [ ] Lint clean
- [ ] Type check clean
- [ ] Security scan clean
- [ ] Performance benchmarks met
- [ ] Narrative summary generated
- [ ] Metrics logged
- [ ] Token budget respected
- [ ] No regressions
- [ ] Elite standards met (if elite mode)

## Anti-Patterns to Avoid

❌ **Don't:**
- Execute without planning
- Skip testing
- Ignore token limits
- Use sequential when parallel possible
- Generate mock/placeholder code
- Skip validation gates
- Over-orchestrate simple tasks

✅ **Do:**
- Plan before executing
- Test continuously
- Monitor token usage
- Parallelize aggressively
- Ensure production-ready code
- Enforce quality gates
- Use right-sized orchestration

---

**Benchmark Standards:**
- Palantir Gotham: Multi-domain intelligence
- CrowdStrike Falcon: Real-time security
- Darktrace: AI-powered threat detection
- Grafana: Sophisticated visualization
- Datadog: Comprehensive observability

**Token Efficiency:**
- Default: 60-70% vs manual
- Advanced: 70-80% vs manual
- Elite: 80-90% vs manual (with lazy loading)

**Success Rate:**
- 99%+ for default tasks
- 95%+ for advanced tasks
- 90%+ for elite tasks (due to complexity)

---
**Version**: 2.0-Elite
**Last Updated**: 2025-11-08
**Status**: Production-Ready
**Impact**: 3-5x faster execution vs sequential workflows

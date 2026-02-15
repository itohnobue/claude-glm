# GLM Models Reference

## Available Models

| Model | Input $/MTok | Output $/MTok | Context | Notes |
|-------|-------------|--------------|---------|-------|
| **GLM-5** | $1.00 | $3.20 | 200K | Flagship 745B MoE, rivals Claude Opus |
| **GLM-5-Code** | $1.20 | $5.00 | 200K | Code-optimized variant of GLM-5 |
| **GLM-4.7** | $0.60 | $2.20 | 128K | Strong coding model |
| **GLM-4.6** | $0.60 | $2.20 | 128K | Advanced agentic/reasoning/coding |
| **GLM-4.5** | $0.60 | $2.20 | 128K | Stable general-purpose |
| **GLM-4.5-Air** | $0.20 | $1.10 | 128K | Budget option |
| **GLM-4.7-FlashX** | $0.07 | $0.40 | 128K | Ultra-budget |
| **GLM-4.7-Flash** | Free | Free | 128K | Free tier |
| **GLM-4.5-Flash** | Free | Free | 128K | Free tier |

Pricing as of February 2026. Check https://docs.z.ai/guides/overview/pricing for current rates.

## GLM Coding Plan Tiers

| Plan | Price | Prompts / 5h | GLM-5 Access | Weekly Quota |
|------|-------|-------------|-------------|-------------|
| **Lite** | ~$3/mo | ~80 | Not yet | Rolling 7-day |
| **Pro** | ~$15/mo | ~400 | Yes | Rolling 7-day |
| **Max** | Higher | ~1,600 | Yes | Rolling 7-day |

Subscribe at: https://z.ai/subscribe

## Default Mappings by Plan

### Max Plan

Best models at each tier. Requires Max subscription for GLM-5 access.

| Claude Alias | GLM Model | Why |
|-------------|-----------|-----|
| opus | glm-5 | Flagship — best quality, 745B MoE |
| sonnet | glm-4.7 | Strong mid-tier for daily use |
| haiku | glm-4.6 | Lighter but still capable |

### Pro Plan

Strong models without the Max price tag. GLM-5 available but not default to conserve quota.

| Claude Alias | GLM Model | Why |
|-------------|-----------|-----|
| opus | glm-4.7 | Best balance of quality and speed |
| sonnet | glm-4.6 | Good agentic/reasoning capability |
| haiku | glm-4.5 | Budget-friendly general use |

### Lite Plan

Budget-oriented with good performance.

| Claude Alias | GLM Model | Why |
|-------------|-----------|-----|
| opus | glm-4.7 | Best available on Lite |
| sonnet | glm-4.6 | Mid-tier capability |
| haiku | glm-4.5-air | Cheapest paid option |

## Custom Mappings

You can override any mapping by editing the wrapper script:

**macOS/Linux** (`~/.local/bin/claude-glm`):
```bash
export ANTHROPIC_DEFAULT_OPUS_MODEL="glm-5-code"
export ANTHROPIC_DEFAULT_SONNET_MODEL="glm-5"
export ANTHROPIC_DEFAULT_HAIKU_MODEL="glm-4.7"
```

**Windows** (`%USERPROFILE%\.local\bin\claude-glm.cmd`):
```cmd
set "ANTHROPIC_DEFAULT_OPUS_MODEL=glm-5-code"
set "ANTHROPIC_DEFAULT_SONNET_MODEL=glm-5"
set "ANTHROPIC_DEFAULT_HAIKU_MODEL=glm-4.7"
```

## Model Selection Tips

- Use **GLM-5** for complex reasoning, architecture decisions, and multi-step coding
- Use **GLM-4.7** for everyday coding — fast and capable
- Use **GLM-4.6** for agentic workflows and tool use
- Use **GLM-4.5-Air** when speed matters more than depth
- Use **GLM-4.7-Flash** for quick lookups (free, but lower quality)

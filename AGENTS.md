# PJ-LARRY-fo-lmf4.1

Fork personal de `nixfred/lmf4.1`: framework de memoria persistente para agentes (hooks, MCP, CLI). Los cambios propios entran por PR a `personal`. La rama `upstream` es un espejo que mantiene el workflow `sync-personal-fork` (ADR 0024 de `robert-flo/fleet`), que cada día rebasa `personal` sobre ella. Nunca push, PR ni issue al upstream.

## Agentes

- **PM: Sura**, el agente principal de `cursor-agent`. Convierte lo que pide Robert en issues `ready-for-agent`, lanza a `wk-fo-lmf41` y a `rv-fo-lmf41` como subagentes y sigue cada issue hasta su PR.
- **`wk-fo-lmf41`** (`.cursor/agents/wk-fo-lmf41.md`): toma un issue y lo lleva a un PR con prueba real.
- **`rv-fo-lmf41`** (`.cursor/agents/rv-fo-lmf41.md`): revisa el PR en solo lectura antes del merge.

## Agent skills

### Issue tracker

GitHub Issues via gh CLI. External PRs are not triaged. See docs/agents/issue-tracker.md.
Prefix issue titles with the issue number and a separator: <number> - <descriptive title>.

### Triage labels

Canonical five-role triage vocabulary (needs-triage, needs-info, ready-for-agent, ready-to-merge, wontfix). See docs/agents/triage-labels.md.

### Domain docs

Single-context repo layout (GLOSSARY.md + docs/adr/ at repo root). See docs/agents/domain.md.

# k6 — Design System

> Load testing for engineering teams.

k6 (now Grafana k6) is an open-source load-testing tool and cloud service that makes performance testing easy for developers and QA engineers. You script tests in JavaScript, run them from the CLI or the cloud, and get a dense terminal summary of every metric — `http_req_duration`, `http_reqs`, `checks`, `vus`, `iterations`.

The brand is confidently **purple** on soft lavender-tinted surfaces, with a cyan spark for accents and data. It's a developer tool that still feels friendly: rounded geometric type, generous purple, and the unmistakable k6 triangle mark.

---

## Color

### Brand
| Token | Hex | Usage |
|---|---|---|
| k6 purple | `#7D64FF` | Primary brand, mark, CTAs, VU series |
| purple deep | `#6A25F4` | Pressed / darker fills |
| indigo | `#4834B2` | Deep purple accents |
| violet | `#8B55F6` | Secondary purple |
| magenta | `#C055F6` | Gradient partner / highlight |
| cyan | `#00CDFF` | Spark accent — throughput, links, data |
| blue | `#3C72DD` | Tertiary data series |

### Surfaces
| Token | Light | Dark | Usage |
|---|---|---|---|
| canvas | `#F9F8FC` | `#0E0A1F` | Page background (warm lavender / deep purple-black) |
| raised | `#ECE8F1` | `#1A1530` | Recessed surface |
| panel | `#FFFFFF` | `#17122B` | Cards, panels |
| border | `#E2E2E9` | `#47476B` | Hairlines |

### Text
| Token | Light | Dark |
|---|---|---|
| primary | `#3C3C64` | `#ECE8F1` |
| secondary | `#5A5C87` | `#BEB9D7` |
| faint | `#626284` | `#8B87A8` |

### Semantic (test results)
| State | Hex | Meaning |
|---|---|---|
| pass | `#31C48D` | check passed, threshold met |
| fail | `#FF4D6A` | check failed, threshold breached |
| ramp | `#7D64FF` | virtual users (VUs) |
| throughput | `#00CDFF` | requests / sec, rates |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display + UI + body | **TT Pro** ≈ **Rubik** | k6 self-hosts TT Pro (`tt-pro-regular/medium/bold`), but it's CORS-locked — Rubik is the documented geometric fallback. Headings, body, labels, buttons. |
| Code / CLI / metrics | **JetBrains Mono** | k6 scripts (JavaScript), terminal summary, metric values, `p(95)`, timestamps. |

Scale: hero 48–56px `700`, section 22px, metric value 26–34px mono, body 15px, labels 11px uppercase, mono 12–13px.

---

## Shape, spacing & motion

- **Radius:** cards `12px`, tiles `8px`, buttons `8px`, pills `9999px`. Friendly but not consumer-soft.
- **Spacing:** 8px grid; result panels are dense (metrics tables want tight rows).
- **Elevation:** soft purple-tinted shadows on light (`0 10px 30px rgba(125,100,255,.12)`); on dark, borders carry the structure.
- **Motion:** the run *ramps* — VUs climb through stages, the chart draws left-to-right, throughput counters tick up, then the summary lands. Deterministic, functional, ~fast (the test progressing is the animation).

---

## Components

- **Test script** — a JavaScript code block using the real k6 API: `import http from 'k6/http'`, `export const options = { stages: [...] }`, `check(res, {...})`.
- **VU ramp chart** — virtual users over time as a purple area, throughput (req/s) as a cyan line, with a stage timeline (ramp-up → hold → ramp-down).
- **Metric tiles** — big mono value + label: VUs, req/s, p95, iterations.
- **Summary** — the k6 terminal digest: `checks`, `http_req_duration` (avg/min/med/p90/p95), `http_reqs`, `iterations`, `data_received`, each with a pass/fail glyph.

---

## Guardrails

**Do**
- Lead with k6 purple (`#7D64FF`) on lavender-tinted surfaces; use cyan (`#00CDFF`) as the data spark.
- Show the real k6 metric vocabulary: `http_req_duration`, `p(95)`, `checks`, `vus`, `iterations`, `thresholds`.
- Color results by state — green pass, red fail — and keep VUs purple, throughput cyan.
- Script examples in JavaScript with the genuine k6 module API.

**Don't**
- Use pure white or pure black backgrounds — the canvas is warm lavender (`#F9F8FC`) / deep purple (`#0E0A1F`).
- Invent metric names — use k6's actual output fields.
- Overuse cyan; it's a spark for data, not a second brand color.
- Fake a load curve — VUs ramp through defined stages; throughput follows the ramp.

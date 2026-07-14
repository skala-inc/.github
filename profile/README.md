<p align="center">
  <img src="img/logo.png" alt="Skala" width="120" />
</p>

<h1 align="center">Skala</h1>

<p align="center">
  Real-time abuse detection for modern SaaS.<br/>
  Stop fake signups, trial abuse, and automated attacks before they hit your backend.
</p>

---

## What We Build

Skala is an API that scores events like **signups, logins, and checkouts** and returns a risk score in real time.

```
ALLOW   → 0–39
STEP_UP → 40–69
BLOCK   → 70–100
```

```json
{
  "risk_score": 87,
  "decision": "block",
  "reason_codes": ["SIG_IP_VELOCITY", "SIG_DEVICE_REUSE"]
}
```

---

## SDKs

| Package | Description |
|---------|-------------|
| [ts-sdk](https://github.com/skala-inc/ts-sdk) | TypeScript / Node SDK |
| [py-sdk](https://github.com/skala-inc/py-sdk) | Python SDK |
| [go-sdk](https://github.com/skala-inc/go-sdk) | Go SDK |
| [browser-sdk](https://github.com/skala-inc/browser-sdk) | Browser SDK |

---

## Quick Start

```ts
import { createSkalaClient } from "@skala/ts-sdk"

const skala = createSkalaClient({
  apiKey: process.env.SKALA_API_KEY
})

const result = await skala.score({
  event: "signup",
  ip: req.ip,
  email: user.email
})
```

---

## Links

- [Website](https://skala.dev)
- [Documentation](https://docs.skala.dev)
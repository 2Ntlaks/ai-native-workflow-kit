# Security And Permissions

Autonomy level says what the agent may decide. Permission policy says what the agent may touch.

| Action | Default Policy |
|---|---|
| Read repository files | Allowed unless private data is involved |
| Edit scoped source files | Allowed at A2+ |
| Run tests and local builds | Allowed unless destructive or external |
| Install dependencies | Ask first |
| Edit configuration | Ask first |
| Touch database migrations | Ask first |
| Delete files | Ask first |
| Run network commands | Ask first unless research policy allows it |
| Modify auth/security code | Ask first |
| Commit changes | Ask first unless explicitly requested |
| Broad refactor | Ask first |

Sensitive areas include auth, payments, secrets, private data, migrations, deployment, CI, and embedded code that can affect hardware.

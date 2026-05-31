# Security Review

Use whenever the task touches data, permissions, dependencies, network access, deployment, auth, or embedded hardware behavior.

- [ ] No secrets, tokens, keys, or private data were added to the repo.
- [ ] Auth, authorization, and role changes are explicit and reviewed by the human.
- [ ] New dependencies or network behavior are approved and justified.
- [ ] Database migrations are approved, reversible where possible, and tested against representative data.
- [ ] Destructive commands or file deletions were explicitly authorized.
- [ ] Embedded or hardware-facing changes describe failure mode and manual safety check.
- [ ] Remaining security risk is listed in the review packet.

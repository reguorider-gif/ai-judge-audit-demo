# AI Judge Audit Demo

AI Judge is a source-isolated Loop QA and audit/report layer for agent, LLM-as-judge, RAG evaluation, and trace review workflows.

This public demo shows the artifact AI Judge is designed to produce:

- trigger, handoff, verification, memory, and next-run review structure
- claim-level support and contradiction mapping
- judge-seat agreement and dissent summary
- reviewer-ready verdict packet
- lightweight JSON handoff shape for eval and observability tools
- Markdown and GitHub issue-shaped handoffs for review queues
- a portable JSON packet contract in `sample-loop-packet.json`

Primary collaboration ask:
send one failed or borderline agent/eval loop and get back one reviewer-ready Loop QA packet.

Public sample packet:
https://gist.github.com/reguorider-gif/c5f4e3b5731cd51366dd7c214e8c70e8

No private user data, credentials, or production traces are included.

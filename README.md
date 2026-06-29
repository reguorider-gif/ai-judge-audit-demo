# AI Judge Audit Demo

Drop a high-risk claim. Get an auditable verdict.

AI Judge is not a smarter-answer demo. It is responsibility infrastructure for high-risk, ambiguous judgments where a team needs evidence, dissent, a human signature, and an archived decision.

This MVP only does four things:

- `Radar Card`: decide whether the problem is worth judging.
- `Problem Contract`: lock the problem, wrong-decision cost, signer, and acceptance criteria.
- `Verdict Packet`: collect multi-model judgments, evidence chain, dissent, and overclaim findings.
- `Final Report`: produce a human-signable, traceable, archivable verdict.

The frontend intentionally stays small. It only surfaces whether the issue is worth judging, why it is worth judging, the verdict, evidence chain, dissent, and human signature state. The deeper product contract lives in `sample-loop-packet.json` and `AI_Judge_Audit_Sample_Report.html`.

Public sample packet:
https://gist.github.com/reguorider-gif/c5f4e3b5731cd51366dd7c214e8c70e8

No private user data, credentials, or production traces are included.

# SAFE-Triage

Research code for **SAFE-Triage: Evidence-gated routing of smart-contract vulnerability reports**.

## Download and reproduce

The complete code release is distributed as [SAFE-Triage_Source.zip](SAFE-Triage_Source.zip)
(126 files). Download and extract the archive, then run:

```bash
cd safe-triage
python3 scripts/verify_public_release.py
```

This command needs only Python 3.11+ and performs an offline numerical replay.
It checks every included file against the SHA-256 manifest and reproduces all
three statistical JSON outputs. The archive's README provides installation,
unit-test, figure-generation, and fresh-inference instructions.

Archive SHA-256: `35decda1fd5cb1c95dd743665ab7e61c8dafcc0b1d4dd2b3306bbad052cdd993`

## Contents

Data-preparation and inference code; supervised, OSP-style and StruQ comparators;
gate and uncertainty analysis; paired attack experiments; historical monitoring;
44 unit tests; figure/table generators; derived decision records; aggregate
results; prompts and data-access instructions. The five main LLMs range from
3.8B to 70B parameters and the study uses six historical datasets from four platforms.

SAFE-Triage checks whether a proposed automatic route meets decision and evidence
conditions. Failed checks leave routing to a human. Both automatic routes still
lead to human review. Its measured benefit is reduced action on targeted integrity
failures, not improved clean classification or universal attack resistance.

## Data and license

Third-party reports, contract source code, model weights, raw model responses,
private files and credentials are excluded. The archive documents how source
inputs are obtained separately. Exact offline numerical replay is supported;
fresh inference additionally requires those source inputs and model checkpoints.
No open-source license has yet been assigned to the research code. Third-party
materials retain their original terms. See `THIRD_PARTY_NOTICE.md` in the archive.

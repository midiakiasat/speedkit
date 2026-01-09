# VERIFRAX

This repository is the authoritative specification for VERIFRAX.

VERIFRAX executes verification operations on input data.

## Execution Endpoint

https://verifrax.net

## Termination Conditions

System terminates when verification operation completes. System terminates when verification operation fails. System terminates when input validation fails.

## What This System Does NOT Do

- Does not execute support operations
- Does not execute feature modifications
- Does not execute third-party integrations
- Does not store data after execution terminates

## Output

System produces verification certificates as files. System produces status reports as files. Files contain verification results and timestamps.

## Access

Execution is publicly accessible. Input validation occurs before execution begins.

## Archive

After termination, system outputs remain accessible. System code does not execute after termination. Execution artifacts are produced at termination. Long-term retention is defined by this repository.

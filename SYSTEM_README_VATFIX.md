# VATFIX

This repository is the authoritative specification for VATFIX.

VATFIX executes VAT document correction operations on input files.

## Execution Endpoint

https://sepa.vatfix.eu

## Termination Conditions

System terminates when correction operation completes. System terminates when correction operation fails. System terminates when input validation fails.

## What This System Does NOT Do

- Does not execute support operations
- Does not execute feature modifications
- Does not execute third-party integrations
- Does not store data after execution terminates

## Output

System produces corrected VAT documents as files. System produces validation reports as files. Files contain correction results and timestamps.

## Access

Execution is publicly accessible. Input validation occurs before execution begins.

## Archive

After termination, system outputs remain accessible. System code does not execute after termination. Execution artifacts are produced at termination. Long-term retention is defined by this repository.

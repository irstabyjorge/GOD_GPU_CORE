# PETS / AEGIS IP Shield — Coverage Charter

**Purpose:** additive preservation, provenance, integrity monitoring, attribution, and safe error/omission handling for this repository and its declared assets.

**Coverage is technical, not contractual.** This charter is not an insurance policy, surety bond, indemnity, copyright registration, legal opinion, or guarantee of exclusivity or recovery.

## Master architecture and scope
PETS remains the master architecture. AEGIS OMEGA / IP Shield is a cross-cutting protection layer. This repository's source code, documentation, configuration, schemas, tests, workflows, releases, model/data references, and approved derivative artifacts may be inventoried when explicitly in scope. Existing architecture and modules remain intact.

## Additive-only preservation
- Never delete, rename, overwrite, force-push, or replace existing assets during protection work.
- Add records, manifests, snapshots, and documentation alongside existing material.
- If a target path exists, preserve it; create a versioned evidence record rather than updating it.
- Preserve source history and record base revision, incoming revision, merge commit, and any conflict resolution.
- Do not alter access controls, visibility, billing, licensing, runtime settings, model weights, datasets, or production services.
- Never silently omit an asset because it is inaccessible, unsupported, or failed to scan.

## Evidence and provenance
Record where available: platform, owner, repository ID/type, path, revision, parent revision, file size, platform blob IDs, provider LFS digests, independently computed SHA-256 (only when bytes were actually obtained and hashed), declared contributor, timestamps, source URL, collection time/method, license metadata, manifest digest, custody events, verification status, and limitations.

Keep these categories separate: **observed**, **user-supplied**, **inferred**, **hypothesis**, **symbolic**, and **unknown**. Never promote an inference to a verified fact.

## Errors, omissions, and coverage exceptions
Every run must account for all requested owners, repository types, pages, and assets. Record each result as inventoried, inaccessible, permission denied, not found, unsupported, pagination incomplete, rate-limited, transient failure, metadata missing/inconsistent, integrity mismatch, skipped with reason, or pending human review.

A run is **complete** only when every in-scope item has a terminal status and pagination is exhausted. Partial success is still **partial**. Record safe error classes and correlation IDs; never log credentials, access tokens, or unnecessary personal data. Missing evidence is an explicit gap, not proof that an asset does not exist.

## Integrity controls
Use canonical manifests and SHA-256 digests; append-only, sequence-checked hash-chained audit events; verify the ledger before appending; verify manifests and index anchors before audit or publication; capture drift as new evidence without auto-reverting remote changes; and preserve independent evidence backups. Git blob IDs are SHA-1. Hub LFS digests are provider metadata unless independently recomputed from retrieved bytes. A hash proves identity of the input bytes, not authorship, ownership, originality, creation date, or infringement.

## IP discrepancy and claim handling
For possible reuse, omission, attribution error, license conflict, or unexplained change: preserve the exact asset/version/URL and timestamp; record reproducible comparisons; preserve relevant licenses and contribution records; classify as confirmed technical discrepancy, possible rights issue, or unresolved report; require human/legal review before external allegations or notices; and record any resolution as a new append-only event.

## Safe operation
Operate only on assets/accounts the operator owns or is authorized to inspect. Scheduled automation uses read-only credentials. Keep write credentials out of CI, source, logs, and artifacts. Any remote write requires separate explicit approval, a verified baseline, reviewed diff, and no-overwrite check. No covert collection, unauthorized access, mass surveillance, credential harvesting, or destructive response.

## Limits
The shield cannot prevent copying, platform-side deletion, account compromise, administrator actions, or lawful reuse under applicable licenses. Metadata-only inventory does not prove model or dataset contents. The system does not guarantee recovery, indemnification, or legal rights.

## Release gate
Do not label coverage deployed or complete until tests pass, changes are reviewed and merged, every in-scope asset has a status, evidence is verified and independently backed up, exceptions are disclosed, and automated remote writes remain disabled unless separately authorized.

# AEGIS GitHub IP SHIELD

Runs on pushes, pull requests, manual dispatches and a weekly schedule. Records commit/tree IDs, refs, up to 25,000 tracked file paths and SHA-256 fingerprints, plus up to 500 commit metadata entries (email represented by a hash). Uploads a JSON report and checksum as a 90-day GitHub Actions artifact; non-PR runs also save a versioned copy to `ip-shield-ledger`.

Requires GitHub Actions and a workflow token allowed to write repository contents. Organization or branch policies can block ledger writes while artifact upload still works.

Limits: Git author/time fields are declared metadata, not verified identity or trusted time. Hashes identify bytes, not authorship, originality, ownership or infringement. No source contents are copied into the report. The ledger branch is versioned, not immutable. Third-party/joint contributions retain their rights and licenses. This workflow only covers this repository and triggered refs; it does not register IP or revoke third-party rights.

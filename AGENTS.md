# youtube-dl

Upstream-style command-line downloader repository. Minimize local divergence and preserve upstream-compatible behavior.

## Commands
- Use the repository's existing test/build instructions from README/CONTRIBUTING.
- Run focused extractor/downloader tests for touched behavior before broader suites.

## Shared rules
- Do not introduce project-wide rewrites for a focused upstream-compatible fix.
- Preserve CLI/output behavior unless the task explicitly changes the public contract.
- Test network/provider parsing with existing fixtures/mocks when possible; live site behavior is unstable.
- Do not commit downloaded media, cookies, account credentials, or session data.
- Keep license/upstream attribution intact.

## Change-dependent checks
- Extractor/parser: focused fixture tests plus relevant upstream suite.
- CLI/core: public-contract tests.
- Packaging: use repository release/build procedure only when requested.

## Done
- Relevant upstream-style tests pass.
- Local change remains narrowly attributable.
- No credentials/downloaded private media are included.

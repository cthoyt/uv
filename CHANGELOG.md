# Changelog

## 0.5.26

### Enhancements

- Add support for `uvx python` ([#11076](https://github.com/astral-sh/uv/pull/11076))
- Allow `--no-dev --invert` in `uv tree` ([#11068](https://github.com/astral-sh/uv/pull/11068))
- Update `uv python install --reinstall` to reinstall all previous versions ([#11072](https://github.com/astral-sh/uv/pull/11072))
- Consistently write log messages with capitalized first word ([#11111](https://github.com/astral-sh/uv/pull/11111))
- Suggest `--build-backend` when `--backend` is passed to `uv init` ([#10958](https://github.com/astral-sh/uv/pull/10958))
- Improve retry trace message ([#11108](https://github.com/astral-sh/uv/pull/11108))

### Performance

- Remove unnecessary UTF-8 conversion in hash parsing ([#11110](https://github.com/astral-sh/uv/pull/11110))

### Bug fixes

- Ignore non-hash fragments in HTML API responses ([#11107](https://github.com/astral-sh/uv/pull/11107))
- Avoid resolving symbolic links when querying Python interpreters ([#11083](https://github.com/astral-sh/uv/pull/11083))
- Avoid sharing state between universal and non-universal resolves ([#11051](https://github.com/astral-sh/uv/pull/11051))
- Error when `--script` is passing a non-PEP 723 script ([#11118](https://github.com/astral-sh/uv/pull/11118))
- Make metadata deserialization failures non-fatal in the cache ([#11105](https://github.com/astral-sh/uv/pull/11105))
- Mark metadata as dynamic when reading from built wheel cache ([#11046](https://github.com/astral-sh/uv/pull/11046))
- Propagate credentials for `<index>/simple` to `<index>/...` endpoints ([#11074](https://github.com/astral-sh/uv/pull/11074))
- Fix conflicting extra bug during `uv sync` ([#11075](https://github.com/astral-sh/uv/pull/11075))

### Documentation

- Add PyTorch XPU instructions to the PyTorch guide ([#11109](https://github.com/astral-sh/uv/pull/11109))
- Add docs for signal handling ([#11041](https://github.com/astral-sh/uv/pull/11041))
- Explain build frontend vs. build backend ([#11094](https://github.com/astral-sh/uv/pull/11094))
- Fix formatting of `RUST_LOG` documentation ([#10053](https://github.com/astral-sh/uv/pull/10053))
- Fix typo in `--no-deps` description ([#11073](https://github.com/astral-sh/uv/pull/11073))
- Reflow CLI documentation comments ([#11040](https://github.com/astral-sh/uv/pull/11040))
- Shorten "Using existing Python versions" nav item so it fits on one line ([#11077](https://github.com/astral-sh/uv/pull/11077))
- Some minor touch-ups to the Python install guide ([#11116](https://github.com/astral-sh/uv/pull/11116))
- Update Dependabot tracking issue link ([#11054](https://github.com/astral-sh/uv/pull/11054))
- Update documentation for running in a container ([#11052](https://github.com/astral-sh/uv/pull/11052))
- Upgrade PyTorch version in documentation ([#11114](https://github.com/astral-sh/uv/pull/11114))
- Use `sys_platform` in lieu of `platform_system` in PyTorch docs ([#11113](https://github.com/astral-sh/uv/pull/11113))
- Use positive (rather than negative) markers in PyTorch examples ([#11112](https://github.com/astral-sh/uv/pull/11112))
- Fix unnecessary backslashes in brackets ([#11059](https://github.com/astral-sh/uv/pull/11059))
- Suggest setting copy link mode in GitLab integration guide ([#11067](https://github.com/astral-sh/uv/pull/11067))

## 0.5.25

### Enhancements

- Allow installation of manylinux wheels on loongarch64 ([#10927](https://github.com/astral-sh/uv/pull/10927))
- Allow optional `=` for editables in `requirements.txt` ([#10954](https://github.com/astral-sh/uv/pull/10954))
- Add Windows aarch64 to the release binaries ([#10885](https://github.com/astral-sh/uv/pull/10885))

### Bug fixes

- Use spec-compliant (`128+n`) exit codes for `uv run` and `uv tool run` on Unix ([#10781](https://github.com/astral-sh/uv/pull/10781))
- Fix best-interpreter lookups when there is an invalid interpreter in the `PATH` ([#11030](https://github.com/astral-sh/uv/pull/11030))
- Guard against concurrent cache writes on Windows ([#11007](https://github.com/astral-sh/uv/pull/11007))
- Prioritize package preferences with greater package versions ([#10963](https://github.com/astral-sh/uv/pull/10963))
- Reject `--editable` flag on non-directory requirements ([#10994](https://github.com/astral-sh/uv/pull/10994))
- Respect `--no-sources` for `uv pip install` workspace discovery ([#11003](https://github.com/astral-sh/uv/pull/11003))
- Set `JEMALLOC_SYS_WITH_LG_PAGE=16` in ARM Docker builds ([#10943](https://github.com/astral-sh/uv/pull/10943))
- Update `riscv64` Python downloads to allow install on `riscv64gc` ([#10937](https://github.com/astral-sh/uv/pull/10937))
- Fix file persist retries on Windows ([#11008](https://github.com/astral-sh/uv/pull/11008))
- Fix incorrect error message when specifying `tool.uv.sources.(package).workspace` with other options ([#11013](https://github.com/astral-sh/uv/pull/11013))
- Improve SIGINT handling in `uv run` ([#11009](https://github.com/astral-sh/uv/pull/11009))

### Documentation

- Add `SECURITY` policy ([#11035](https://github.com/astral-sh/uv/pull/11035))
- Add `Requires-Python` upper bound behavior to the docs ([#10964](https://github.com/astral-sh/uv/pull/10964))
- Add a troubleshooting section and reproducible example guide ([#10947](https://github.com/astral-sh/uv/pull/10947))
- Add documentation for `uv add -r` ([#10926](https://github.com/astral-sh/uv/pull/10926))
- Amend `requires-python` rules in resolver documentation ([#10993](https://github.com/astral-sh/uv/pull/10993))
- Reference workspaces in `--no-sources` documentation ([#10995](https://github.com/astral-sh/uv/pull/10995))
- Update documentation for activating virtual environments in different shell ([#11000](https://github.com/astral-sh/uv/pull/11000))
- Add Docker SHA pinning tip ([#10955](https://github.com/astral-sh/uv/pull/10955))

## 0.5.24

### Enhancements

- Improve determinism of resolution by always setting package priorities ([#10853](https://github.com/astral-sh/uv/pull/10853))
- Upgrade to `cargo-dist` 0.28.0; improves several installer behaviors ([#10884](https://github.com/astral-sh/uv/pull/10884))

### Performance

- Remove dependencies clone in resolver ([#10880](https://github.com/astral-sh/uv/pull/10880))
- Use Hashbrown's raw entry API to reduce hashes and clone in resolver priority determination ([#10881](https://github.com/astral-sh/uv/pull/10881))

### Bug fixes

- Allow fallback to Python download on non-critical discovery errors ([#10908](https://github.com/astral-sh/uv/pull/10908))

### Preview features

- Register managed Python version with the Windows Registry (PEP 514) ([#10634](https://github.com/astral-sh/uv/pull/10634))

### Documentation

- Improve documentation for some environment variables ([#10887](https://github.com/astral-sh/uv/pull/10887))
- Add git subdirectory example ([#10894](https://github.com/astral-sh/uv/pull/10894))

## 0.5.23

### Enhancements

- Add `--refresh` to `uv venv` ([#10834](https://github.com/astral-sh/uv/pull/10834))
- Add `--no-default-groups` command-line flag ([#10618](https://github.com/astral-sh/uv/pull/10618))

### Bug fixes

- Sort extras and groups when comparing lockfile requirements ([#10856](https://github.com/astral-sh/uv/pull/10856))
- Include `commit_id` and `requested_revision` in `direct_url.json` ([#10862](https://github.com/astral-sh/uv/pull/10862))
- Invalidate lockfile when static versions change ([#10858](https://github.com/astral-sh/uv/pull/10858))
- Make GitHub fast path errors non-fatal ([#10859](https://github.com/astral-sh/uv/pull/10859))
- Remove warnings for `--frozen` and `--locked` in `uv run --script` ([#10840](https://github.com/astral-sh/uv/pull/10840))
- Resolve `find-links` paths relative to the configuration file ([#10827](https://github.com/astral-sh/uv/pull/10827))
- Respect visitation order for proxy packages ([#10833](https://github.com/astral-sh/uv/pull/10833))
- Treat version mismatch errors as non-fatal in fast paths ([#10860](https://github.com/astral-sh/uv/pull/10860))
- Mark `--locked` and `--upgrade` are conflicting ([#10836](https://github.com/astral-sh/uv/pull/10836))
- Relax error checking around unconditional enabling of conflicting extras ([#10875](https://github.com/astral-sh/uv/pull/10875))

### Documentation

- Reduce ambiguity in conflicting extras example ([#10877](https://github.com/astral-sh/uv/pull/10877))
- Update pre-commit documentation  ([#10756](https://github.com/astral-sh/uv/pull/10756))

### Error messages

- Error when workspace contains conflicting Python requirements ([#10841](https://github.com/astral-sh/uv/pull/10841))
- Improve uvx error message when uv is missing ([#9745](https://github.com/astral-sh/uv/pull/9745))

## 0.5.22

### Enhancements

- Include version and contact information in GitHub User Agent ([#10785](https://github.com/astral-sh/uv/pull/10785))

### Performance

- Add fast-path for recursive extras in dynamic validation ([#10823](https://github.com/astral-sh/uv/pull/10823))
- Fetch `pyproject.toml` from GitHub API ([#10765](https://github.com/astral-sh/uv/pull/10765))
- Remove allocation in Git SHA truncation ([#10801](https://github.com/astral-sh/uv/pull/10801))
- Skip GitHub fast path when full commit is already known ([#10800](https://github.com/astral-sh/uv/pull/10800))

### Bug fixes

- Add fallback to build backend when `Requires-Dist` mismatches ([#10797](https://github.com/astral-sh/uv/pull/10797))
- Avoid deserialization error for paths above the root ([#10789](https://github.com/astral-sh/uv/pull/10789))
- Avoid respecting preferences from other indexes ([#10782](https://github.com/astral-sh/uv/pull/10782))
- Disable the distutils setuptools shim during interpreter query ([#10819](https://github.com/astral-sh/uv/pull/10819))
- Omit variant when detecting compatible Python installs ([#10722](https://github.com/astral-sh/uv/pull/10722))
- Remove TOCTOU errors in Git clone ([#10758](https://github.com/astral-sh/uv/pull/10758))
- Validate metadata under GitHub fast path ([#10796](https://github.com/astral-sh/uv/pull/10796))
- Include conflict markers in fork markers ([#10818](https://github.com/astral-sh/uv/pull/10818))

### Error messages

- Add tag incompatibility hints to sync failures ([#10739](https://github.com/astral-sh/uv/pull/10739))
- Improve log when distutils is missing ([#10713](https://github.com/astral-sh/uv/pull/10713))
- Show non-critical Python discovery errors if no other interpreter is found ([#10716](https://github.com/astral-sh/uv/pull/10716))
- Use colors for lock errors ([#10736](https://github.com/astral-sh/uv/pull/10736))

### Documentation

- Add testing instructions to the AWS Lambda guide ([#10805](https://github.com/astral-sh/uv/pull/10805))

## 0.5.21

### Enhancements

- Avoid building dynamic versions when validating lockfile ([#10703](https://github.com/astral-sh/uv/pull/10703))

### Configuration

- Add `UV_VENV_SEED` environment variable ([#10715](https://github.com/astral-sh/uv/pull/10715))

### Performance

- Store unsupported tags in wheel filename ([#10665](https://github.com/astral-sh/uv/pull/10665))

### Bug fixes

- Avoid attempting to patch macOS dylib for non-macOS installs ([#10721](https://github.com/astral-sh/uv/pull/10721))
- Avoid narrowing `requires-python` marker with disjunctions ([#10704](https://github.com/astral-sh/uv/pull/10704))
- Respect environment variable credentials for indexes outside root ([#10688](https://github.com/astral-sh/uv/pull/10688))
- Respect preferences for explicit index dependencies from `requirements.txt` ([#10690](https://github.com/astral-sh/uv/pull/10690))
- Sort preferences by environment, then index ([#10700](https://github.com/astral-sh/uv/pull/10700))
- Ignore permission errors when looking for user-level configuration file ([#10697](https://github.com/astral-sh/uv/pull/10697))

### Documentation

- Add `SyntaxWarning` compatibility note to bytecode compilation docs ([#10701](https://github.com/astral-sh/uv/pull/10701))
- Add `MACOSX_DEPLOYMENT_TARGET` to the `--python-platform` documentation ([#10698](https://github.com/astral-sh/uv/pull/10698))

## 0.5.20

### Bug fixes

- Avoid failing when deserializing unknown tags ([#10655](https://github.com/astral-sh/uv/pull/10655))

## 0.5.19

### Enhancements

- Filter wheels from lockfile based on architecture ([#10584](https://github.com/astral-sh/uv/pull/10584))
- Omit dynamic versions from the lockfile ([#10622](https://github.com/astral-sh/uv/pull/10622))
- Add support for `pip freeze --path` ([#10488](https://github.com/astral-sh/uv/pull/10488))
- Reduce verbosity of inline-metadata message when using `uv run <script.py>` ([#10588](https://github.com/astral-sh/uv/pull/10588))
- Add opt-in Git LFS support ([#10335](https://github.com/astral-sh/uv/pull/10335))
- Recommend `--native-tls` on SSL errors ([#10605](https://github.com/astral-sh/uv/pull/10605))
- Show expected and available ABI tags in resolver errors ([#10527](https://github.com/astral-sh/uv/pull/10527))
- Show target Python version in error messages ([#10582](https://github.com/astral-sh/uv/pull/10582))
- Add `--output-format=json` support to `uv python list` ([#10596](https://github.com/astral-sh/uv/pull/10596))

### Python

The managed Python distributions have been updated, including:

- Python 3.14 support on Windows
- Python 3.14.0a4 support
- 64-bit RISC-V Linux support
- Bundled `libedit` updated from 20210910-3.1 -> 20240808-3.1
- Bundled `tcl/tk` updated from 8.6.12 -> 8.6.14 (for all Python versions on Unix, only for Python 3.14 on Windows)

See the [`python-build-standalone` release notes](https://github.com/astral-sh/python-build-standalone/releases/tag/20250115) for more details.

### Performance

- Avoid allocating when stripping source distribution extension ([#10625](https://github.com/astral-sh/uv/pull/10625))
- Reduce `WheelFilename` to 48 bytes ([#10583](https://github.com/astral-sh/uv/pull/10583))
- Reduce distribution size to 200 bytes ([#10601](https://github.com/astral-sh/uv/pull/10601))
- Remove `import re` from entrypoint wrapper scripts ([#10627](https://github.com/astral-sh/uv/pull/10627))
- Shrink size of platform tag enum ([#10546](https://github.com/astral-sh/uv/pull/10546))
- Use `ArcStr` in verbatim URL ([#10600](https://github.com/astral-sh/uv/pull/10600))
- Use `memchr` for wheel parsing ([#10620](https://github.com/astral-sh/uv/pull/10620))

### Bug fixes

- Avoid reading symlinks during `uv python install` on Windows ([#10639](https://github.com/astral-sh/uv/pull/10639))
- Correct Pyston tag format ([#10580](https://github.com/astral-sh/uv/pull/10580))
- Provide `pyproject.toml` path for parse errors in `uv venv` ([#10553](https://github.com/astral-sh/uv/pull/10553))
- Don't treat `setuptools` and `wheel` as seed packages in uv sync on Python 3.12 ([#10572](https://github.com/astral-sh/uv/pull/10572))
- Fix git-tag cache-key reader in case of slashes (#10467) ([#10500](https://github.com/astral-sh/uv/pull/10500))
- Include build tag in rendered wheel filenames ([#10599](https://github.com/astral-sh/uv/pull/10599))
- Patch embedded install path for Python dylib on macOS during `python install` ([#10629](https://github.com/astral-sh/uv/pull/10629))
- Read cached registry distributions when `--config-settings` are present ([#10578](https://github.com/astral-sh/uv/pull/10578))
- Show resolver hints for packages with markers ([#10607](https://github.com/astral-sh/uv/pull/10607))

### Documentation

- Add meta titles to documents in guides, excluding integration documents ([#10539](https://github.com/astral-sh/uv/pull/10539))
- Remove `build-system` from example workspace rot ([#10636](https://github.com/astral-sh/uv/pull/10636))

### Preview features

- Make build backend type annotations more generic ([#10549](https://github.com/astral-sh/uv/pull/10549))

## 0.5.18

### Bug fixes

- Avoid forking for identical markers ([#10490](https://github.com/astral-sh/uv/pull/10490))
- Avoid panic in `uv remove` when only comments exist ([#10484](https://github.com/astral-sh/uv/pull/10484))
- Revert "improve shell compatibility of venv activate scripts (#10397)" ([#10497](https://github.com/astral-sh/uv/pull/10497))

## 0.5.17

This release includes support for generating lockfiles from scripts based on inline metadata, as defined in PEP 723.

By default, scripts remain unlocked, and must be locked explicitly with `uv lock --script /path/to/script.py`, which
will generate a lockfile adjacent to the script (e.g., `script.py.lock`). Once generated, the lockfile will be
respected (and updated, if necessary) across `uv run --script`, `uv add --script`, and `uv remove --script` invocations.

This release also includes support for `uv export --script` and `uv tree --script`. Both commands support PEP 723
scripts with and without accompanying lockfiles.

### Enhancements

- Add support for locking PEP 723 scripts ([#10135](https://github.com/astral-sh/uv/pull/10135))
- Respect PEP 723 script lockfiles in `uv run` ([#10136](https://github.com/astral-sh/uv/pull/10136))
- Update PEP 723 lockfile in `uv add --script` ([#10145](https://github.com/astral-sh/uv/pull/10145))
- Update PEP 723 lockfile in `uv remove --script` ([#10162](https://github.com/astral-sh/uv/pull/10162))
- Add `--script` support to `uv export` for PEP 723 scripts ([#10160](https://github.com/astral-sh/uv/pull/10160))
- Add `--script` support to `uv tree` for PEP 723 scripts ([#10159](https://github.com/astral-sh/uv/pull/10159))
- Add `ls` alias to `uv {tool, python, pip} list` ([#10240](https://github.com/astral-sh/uv/pull/10240))
- Allow reading `--with-requirements` from stdin in `uv add` and `uv run` ([#10447](https://github.com/astral-sh/uv/pull/10447))
- Warn-and-ignore for unsupported `requirements.txt` options ([#10420](https://github.com/astral-sh/uv/pull/10420))

### Preview features

- Add remaining Python type annotations to build backend ([#10434](https://github.com/astral-sh/uv/pull/10434))

### Performance

- Avoid allocating for names in the PEP 508 parser ([#10476](https://github.com/astral-sh/uv/pull/10476))
- Fetch concurrently for non-first-match index strategies ([#10432](https://github.com/astral-sh/uv/pull/10432))
- Remove unnecessary `.to_string()` call ([#10419](https://github.com/astral-sh/uv/pull/10419))
- Respect sentinels in package prioritization ([#10443](https://github.com/astral-sh/uv/pull/10443))
- Use `ArcStr` for marker values ([#10453](https://github.com/astral-sh/uv/pull/10453))
- Use `ArcStr` for package, extra, and group names ([#10475](https://github.com/astral-sh/uv/pull/10475))
- Use `matches!` rather than `contains` in `requirements.txt` parsing ([#10423](https://github.com/astral-sh/uv/pull/10423))
- Use faster disjointness check for markers ([#10439](https://github.com/astral-sh/uv/pull/10439))
- Pre-compute PEP 508 markers from universal markers ([#10472](https://github.com/astral-sh/uv/pull/10472))

### Bug fixes

- Fix `UV_FIND_LINKS` delimiter to split on commas ([#10477](https://github.com/astral-sh/uv/pull/10477))
- Improve `uv tool list` output when tool environment is broken ([#10409](https://github.com/astral-sh/uv/pull/10409))
- Only track markers for compatible versions ([#10457](https://github.com/astral-sh/uv/pull/10457))
- Respect `requires-python` when installing tools ([#10401](https://github.com/astral-sh/uv/pull/10401))
- Visit proxy packages eagerly ([#10441](https://github.com/astral-sh/uv/pull/10441))
- Improve shell compatibility of `venv` activate scripts ([#10397](https://github.com/astral-sh/uv/pull/10397))
- Read publish username from URL ([#10469](https://github.com/astral-sh/uv/pull/10469))

### Documentation

- Add Lambda layer instructions to AWS Lambda guide ([#10411](https://github.com/astral-sh/uv/pull/10411))
- Add `uv lock --script` to the docs ([#10414](https://github.com/astral-sh/uv/pull/10414))
- Use Windows-specific instructions in Jupyter guide ([#10446](https://github.com/astral-sh/uv/pull/10446))

## 0.5.16

### Enhancements

- Accept full requirements in `uv remove` ([#10338](https://github.com/astral-sh/uv/pull/10338))

### Performance

- Avoid over-counting versions in batch prefetcher ([#10350](https://github.com/astral-sh/uv/pull/10350))
- Deactivate tracing for version-choosing ([#10351](https://github.com/astral-sh/uv/pull/10351))
- Force a niche into `VersionSmall` ([#10385](https://github.com/astral-sh/uv/pull/10385))
- Optimize `requirements_for_extra` ([#10348](https://github.com/astral-sh/uv/pull/10348))
- Re-enable `zlib-ng` on x86 platforms ([#10365](https://github.com/astral-sh/uv/pull/10365))
- Re-enable zlib-ng on all platforms (except s390x, PowerPC, and FreeBSD) ([#10370](https://github.com/astral-sh/uv/pull/10370))
- Remove `[u64; 4]` from small version to move `Arc` to full version ([#10345](https://github.com/astral-sh/uv/pull/10345))
- Shrink `Dist` from 352 to 288 bytes ([#10389](https://github.com/astral-sh/uv/pull/10389))
- Speed up file pins by removing nested hash map ([#10346](https://github.com/astral-sh/uv/pull/10346))
- Buffer file reads in `serde_json::from_reader` ([#10341](https://github.com/astral-sh/uv/pull/10341))

### Bug fixes

- Avoid enforcing project-level required version for `uv self` ([#10374](https://github.com/astral-sh/uv/pull/10374))
- Fix Ruff linting warnings from generated template files for extension modules ([#10371](https://github.com/astral-sh/uv/pull/10371))

### Documentation

- Add AWS Lambda integration guide ([#10278](https://github.com/astral-sh/uv/pull/10278))

## 0.5.15

### Python

The managed Python distributions have been updated, including:

- Python 3.14.0a3 support on macOS and Linux
- Performance improvements
- Fixes to SQLite feature detection

See the [`python-build-standalone` release notes](https://github.com/astral-sh/python-build-standalone/releases/tag/20250106) for more details.

### Enhancements

- Respect `FORCE_COLOR` environment variable ([#10315](https://github.com/astral-sh/uv/pull/10315))

### Performance

- Avoid generating unused hashes during `uv lock` ([#10307](https://github.com/astral-sh/uv/pull/10307))
- Visit source distributions before wheels ([#10291](https://github.com/astral-sh/uv/pull/10291))

### Bug fixes

- Avoid downgrading packages when `--upgrade` is provided ([#10097](https://github.com/astral-sh/uv/pull/10097))
- Extract supported architectures from wheel tags ([#10179](https://github.com/astral-sh/uv/pull/10179))
- Redact new index credentials in `uv add` ([#10329](https://github.com/astral-sh/uv/pull/10329))

### Documentation

- Clarify `exclude-newer` only allows full timestamps in settings documentation ([#9135](https://github.com/astral-sh/uv/pull/9135))
- Tweak script `--no-project` comment ([#10331](https://github.com/astral-sh/uv/pull/10331))
- Update copyright year ([#10297](https://github.com/astral-sh/uv/pull/10297))
- Add instructinos for installing with Scoop ([#10332](https://github.com/astral-sh/uv/pull/10332))

## 0.5.14

### Enhancements

- Add `--exact` flag to `uv run` ([#10198](https://github.com/astral-sh/uv/pull/10198))
- Add `--outdated` support to `uv pip tree` ([#10199](https://github.com/astral-sh/uv/pull/10199))
- Add a required version setting to uv ([#10248](https://github.com/astral-sh/uv/pull/10248))
- Add loongarch64 to supported Python platform tags ([#10223](https://github.com/astral-sh/uv/pull/10223))
- Add manylinux2014 aliases for `--python-platform` ([#10217](https://github.com/astral-sh/uv/pull/10217))
- Add support for Python interpreters on ARMv5TE platforms ([#10234](https://github.com/astral-sh/uv/pull/10234))
- Add support for optional `--description` in `uv init` ([#10209](https://github.com/astral-sh/uv/pull/10209))
- Ignore empty or missing hrefs in Simple HTML ([#10276](https://github.com/astral-sh/uv/pull/10276))
- Patch pkgconfig files after Python install ([#10189](https://github.com/astral-sh/uv/pull/10189))

### Performance

- Actually use jemalloc as alternative allocator ([#10269](https://github.com/astral-sh/uv/pull/10269))
- Parse URLs lazily in resolver ([#10259](https://github.com/astral-sh/uv/pull/10259))
- Use `BTreeMap::range` to avoid iterating over unnecessary versions ([#10266](https://github.com/astral-sh/uv/pull/10266))

### Bug fixes

- Accept directories with space names in `uv init` ([#10246](https://github.com/astral-sh/uv/pull/10246))
- Avoid forking on version in non-universal resolutions ([#10274](https://github.com/astral-sh/uv/pull/10274))
- Avoid stripping query parameters from URLs ([#10253](https://github.com/astral-sh/uv/pull/10253))
- Consider workspace dependencies to be 'direct' ([#10197](https://github.com/astral-sh/uv/pull/10197))
- Detect cyclic dependencies during builds ([#10258](https://github.com/astral-sh/uv/pull/10258))
- Guard against self-deletion in `uv venv` and `uv tool` ([#10206](https://github.com/astral-sh/uv/pull/10206))
- Respect static metadata for already-installed distributions ([#10242](https://github.com/astral-sh/uv/pull/10242))

## 0.5.13

### Bug fixes

- Avoid enforcing URL check on initial publish ([#10182](https://github.com/astral-sh/uv/pull/10182))
- Fix incorrect mismatched constraints reference ([#10184](https://github.com/astral-sh/uv/pull/10184))
- Revert "Update `reqwest` (#10178)" ([#10187](https://github.com/astral-sh/uv/pull/10187))

## 0.5.12

### Enhancements

- Support `uv export` for non-project workspaces ([#10144](https://github.com/astral-sh/uv/pull/10144))
- Set glibc versions for standalone installers ([#10142](https://github.com/astral-sh/uv/pull/10142))
- Allow environment variables to be included in cache keys ([#10170](https://github.com/astral-sh/uv/pull/10170))

### Preview features

- Include extras in `uv-build` `Requires-Dist` metadata ([#10110](https://github.com/astral-sh/uv/pull/10110))
- Use `shutil.which` for the build backend ([#10028](https://github.com/astral-sh/uv/pull/10028))

### Bug fixes

- Always write slash paths to RECORD file ([#10164](https://github.com/astral-sh/uv/pull/10164))
- Add support for subdirectories in direct URLs in `uv.lock` ([#10068](https://github.com/astral-sh/uv/pull/10068))
- Avoid duplicating backslashes in sysconfig parser ([#10063](https://github.com/astral-sh/uv/pull/10063))
- Avoid erroring when subdirectories are provided in `uv add` ([#10095](https://github.com/astral-sh/uv/pull/10095))
- Backtrack to non-local versions when wheels are missing platform support ([#10046](https://github.com/astral-sh/uv/pull/10046))
- Fix mirror script to handle newer metadata format ([#10050](https://github.com/astral-sh/uv/pull/10050))
- Preserve sort when deciding on requirement placement ([#10078](https://github.com/astral-sh/uv/pull/10078))
- Remove redundant alias in `uv init` CLI ([#10124](https://github.com/astral-sh/uv/pull/10124))
- Respect sources credentials in non-project workspaces ([#10125](https://github.com/astral-sh/uv/pull/10125))
- Show non-project dependencies in `uv tree` ([#10149](https://github.com/astral-sh/uv/pull/10149))
- Strip fragment when storing direct URL ([#10093](https://github.com/astral-sh/uv/pull/10093))
- Include hashes for local source archives ([#10080](https://github.com/astral-sh/uv/pull/10080))

### Documentation

- Fix invalid syntax in some sources examples ([#10127](https://github.com/astral-sh/uv/pull/10127))

## 0.5.11

### Enhancements

- Normalize `platform_system` to `sys_platform` ([#9949](https://github.com/astral-sh/uv/pull/9949))
- Improve retry mechanisms on Windows for `copy_atomic` and `write_atomic` ([#10026](https://github.com/astral-sh/uv/pull/10026))
- Add nuance to prefetch logging ([#9984](https://github.com/astral-sh/uv/pull/9984))
- Update to [`python-build-standalone 20241219`](https://github.com/astral-sh/python-build-standalone/releases/tag/20241219)

### Preview features

- Build backend: Preserve executable bits for scripts in distributions ([#10027](https://github.com/astral-sh/uv/pull/10027))
- Build backend: Handle case where `metadata_directory` already contains `dist-info` directory ([#10005](https://github.com/astral-sh/uv/pull/10005))

### Performance

- Batch resolver pre-fetches per fork ([#10029](https://github.com/astral-sh/uv/pull/10029))

### Bug fixes

- Allow `--script` to be provided with `uv run -` ([#10035](https://github.com/astral-sh/uv/pull/10035))
- Allow `uv run` arguments when reading from `stdin` ([#10034](https://github.com/astral-sh/uv/pull/10034))
- Prefer higher Python lower-bounds when forking ([#10007](https://github.com/astral-sh/uv/pull/10007))
- Remove references to deprecated `first-match` ([#10036](https://github.com/astral-sh/uv/pull/10036))

### Documentation

- Add `uv python install --preview` to the documentation ([#10010](https://github.com/astral-sh/uv/pull/10010))
- Fix `uv python install --default` note about multiple requests ([#10011](https://github.com/astral-sh/uv/pull/10011))
- Fix typo in Caching docs ([#10032](https://github.com/astral-sh/uv/pull/10032))
- Remove remaining references to deprecated `first-match` ([#10038](https://github.com/astral-sh/uv/pull/10038))
- Supplement missing separators for `UV_INSTALL_DIR` directions on Windows ([#9507](https://github.com/astral-sh/uv/pull/9507))

## 0.5.10

### Enhancements

- Improve backtracking behavior when packages conflict repeatedly ([#9843](https://github.com/astral-sh/uv/pull/9843))
- Patch Python `sysconfig` values such as `AR` at `ar` install time ([#9905](https://github.com/astral-sh/uv/pull/9905))
- Patch Python `sysconfig` values such as `clang` to `cc` at install time ([#9916](https://github.com/astral-sh/uv/pull/9916))
- Skip `--native-tls` in `pip compile` header ([#9913](https://github.com/astral-sh/uv/pull/9913))
- Add resolver error hint for no-binary and no-build failures ([#9948](https://github.com/astral-sh/uv/pull/9948))
- Improve build error messages ([#9660](https://github.com/astral-sh/uv/pull/9660))
- Reduce redundant Python version incompatibilities in resolver error message ([#9957](https://github.com/astral-sh/uv/pull/9957))
- Reduce redundant enumeration of all package versions in some resolver errors ([#9885](https://github.com/astral-sh/uv/pull/9885))
- Improve display of ranges when pre-releases are not allowed ([#9944](https://github.com/astral-sh/uv/pull/9944))
- Improve error messages for `uv remove` ([#9959](https://github.com/astral-sh/uv/pull/9959))
- Improve phrasing for single term incompatibilities ([#9953](https://github.com/astral-sh/uv/pull/9953))
- Improve styling of `uv remove` dependency hints ([#9960](https://github.com/astral-sh/uv/pull/9960))
- Omit trailing zeros on Python requirements inferred from versions ([#9952](https://github.com/astral-sh/uv/pull/9952))
- Show a concise error message for missing `version` field ([#9912](https://github.com/astral-sh/uv/pull/9912))
- Use the build options value to improve hints for no wheel / source distribution errors ([#9950](https://github.com/astral-sh/uv/pull/9950))

### Bug fixes

- Allow multiple disjoint URLs in overrides ([#9893](https://github.com/astral-sh/uv/pull/9893))
- Include explicit indexes in publish index choice ([#9932](https://github.com/astral-sh/uv/pull/9932))
- Fix Python interpreter detection for 32-bit operating systems on 64-bit hosts ([#9970](https://github.com/astral-sh/uv/pull/9970))

### Documentation

- Fix typo "operation system" ([#9971](https://github.com/astral-sh/uv/pull/9971))
- Clarify uninstallation docs ([#9938](https://github.com/astral-sh/uv/pull/9938))
- Add a note to say that dependencies between workspace members are editable ([#9363](https://github.com/astral-sh/uv/pull/9363))
- Correctly document default value of `fork-strategy` setting ([#9931](https://github.com/astral-sh/uv/pull/9931))
- Use double quotes for Windows support in examples ([#9946](https://github.com/astral-sh/uv/pull/9946))
- Remove `pypy` from top-level pin example ([#9896](https://github.com/astral-sh/uv/pull/9896))
- Update references to `python-build-standalone` to reflect the transferred project ([#9977](https://github.com/astral-sh/uv/pull/9977))
- Use a different Ruff version in documentation ([#9943](https://github.com/astral-sh/uv/pull/9943))
- Change example so it works as-is on `powershell` and `cmd.exe` ([#9903](https://github.com/astral-sh/uv/pull/9903))
- Clarify best practice for Python matrix strategy in GitHub Actions ([#9454](https://github.com/astral-sh/uv/pull/9454))
- Add documentation for `uv-lock` and `uv-export` pre-commit hooks ([#9872](https://github.com/astral-sh/uv/pull/9872))

### Preview features

- Build backend: Fix pre-PEP 639 license files ([#9965](https://github.com/astral-sh/uv/pull/9965))

## 0.5.9

### Enhancements

- Fork version selection based on `requires-python` requirements ([#9827](https://github.com/astral-sh/uv/pull/9827))
- Patch `sysconfig` data at install time ([#9857](https://github.com/astral-sh/uv/pull/9857))
- Remove `-isysroot` when patching sysconfig ([#9860](https://github.com/astral-sh/uv/pull/9860))

### Configuration

- Introduce a `--fork-strategy` preference mode ([#9868](https://github.com/astral-sh/uv/pull/9868))
- Add support for `UV_OFFLINE` ([#9795](https://github.com/astral-sh/uv/pull/9795))

### Bug fixes

- Avoid `panic!()` when current directory does not exist ([#9876](https://github.com/astral-sh/uv/pull/9876))
- Avoid reusing interpreter metadata when running under Rosetta ([#9846](https://github.com/astral-sh/uv/pull/9846))
- Avoid trailing slash when deserializing from lockfile ([#9848](https://github.com/astral-sh/uv/pull/9848))
- Fix bug in terms when collapsing unavailable versions in resolver errors ([#9877](https://github.com/astral-sh/uv/pull/9877))
- Fix suggestion to use `uv help python` on invalid install requests ([#9820](https://github.com/astral-sh/uv/pull/9820))
- Skip root when assessing prefix viability ([#9823](https://github.com/astral-sh/uv/pull/9823))
- Avoid spurious 'Upgraded tool environment' in `uv tool upgrade` ([#9870](https://github.com/astral-sh/uv/pull/9870))

### Rust API

- Upgrade minimum Rust version to 1.83 ([#9815](https://github.com/astral-sh/uv/pull/9815))

### Documentation

- Document the `--fork-strategy` setting ([#9887](https://github.com/astral-sh/uv/pull/9887))

### Preview features

- Build backend: Allow underscores in entrypoints ([#9825](https://github.com/astral-sh/uv/pull/9825))

## 0.5.8

**This release does not include the `powerpc64le-unknown-linux-musl` target due to a build issue. See [#9793](https://github.com/astral-sh/uv/issues/9793) for details. If this change affects you, please file an issue with your use-case.**

### Enhancements

- Omit empty resolution markers in lockfile  ([#9738](https://github.com/astral-sh/uv/pull/9738))
- Add `--install-dir` to to `uv python install` and `uninstall` commands ([#7920](https://github.com/astral-sh/uv/pull/7920))
- Add `--show-urls` and `--only-downloads` to `uv python list` ([#8062](https://github.com/astral-sh/uv/pull/8062))
- Add `uv python list --all-arches` ([#9782](https://github.com/astral-sh/uv/pull/9782))
- Add `uv run --gui-script` flag for running Python scripts with `pythonw.exe` ([#9152](https://github.com/astral-sh/uv/pull/9152))
- Allow `--gui-script` on Unix ([#9787](https://github.com/astral-sh/uv/pull/9787))
- Allow download of Python distribution variants optimized for newer x86_64 microarchitectures ([#9781](https://github.com/astral-sh/uv/pull/9781))
- Allow execution of `pyw` files on Unix ([#9759](https://github.com/astral-sh/uv/pull/9759))
- Allow users to specify URLs in `project.dependencies` and `tool.uv.sources` ([#9718](https://github.com/astral-sh/uv/pull/9718))
- Encode mutually-incompatible pairs of markers ([#9444](https://github.com/astral-sh/uv/pull/9444))
- Improve the error message when a Python install request is not valid ([#9783](https://github.com/astral-sh/uv/pull/9783))
- Preserve directory-level standalone build symlinks ([#9723](https://github.com/astral-sh/uv/pull/9723))
- Add support for `uv publish --index <name>` ([#9694](https://github.com/astral-sh/uv/pull/9694))
- Reframe `--locked` and `--frozen` as `--check` operations for `uv lock` ([#9662](https://github.com/astral-sh/uv/pull/9662))
- Rename Python install scratch directory from `.cache` -> `.temp` ([#9756](https://github.com/astral-sh/uv/pull/9756))
- Enable `uv tool uninstall uv` on Windows ([#8963](https://github.com/astral-sh/uv/pull/8963))
- Improve self-dependency hint to make shadowing clear ([#9716](https://github.com/astral-sh/uv/pull/9716))
- Refactor unavailable metadata to shrink the resolver ([#9769](https://github.com/astral-sh/uv/pull/9769))
- Show 'depends on itself' for proxy packages ([#9717](https://github.com/astral-sh/uv/pull/9717))
- Show a dedicated error for missing subdirectories ([#9761](https://github.com/astral-sh/uv/pull/9761))
- Show a dedicated hint for missing `git+` prefixes ([#9789](https://github.com/astral-sh/uv/pull/9789))

### Performance

- Eagerly error when parsing `pyproject.toml` requirements ([#9704](https://github.com/astral-sh/uv/pull/9704))
- Use copy-on-write when normalizing paths ([#9710](https://github.com/astral-sh/uv/pull/9710))

### Bug fixes

- Avoid enforcing non-conflicts in `uv export` ([#9751](https://github.com/astral-sh/uv/pull/9751))
- Don't drop comments between items in TOML tables ([#9784](https://github.com/astral-sh/uv/pull/9784))
- Don't fail with `--no-build` when static metadata is available ([#9785](https://github.com/astral-sh/uv/pull/9785))
- Don't filter non-patch registry version ([#9736](https://github.com/astral-sh/uv/pull/9736))
- Don't read metadata from stale `.egg-info` files ([#9760](https://github.com/astral-sh/uv/pull/9760))
- Enforce correctness of self-dependencies ([#9705](https://github.com/astral-sh/uv/pull/9705))
- Fix projects's typo in resolver error messages ([#9708](https://github.com/astral-sh/uv/pull/9708))
- Ignore `.` prefixed directories during managed Python installation discovery ([#9786](https://github.com/astral-sh/uv/pull/9786))
- Improve handling of invalid virtual environments during interpreter discovery ([#8086](https://github.com/astral-sh/uv/pull/8086))
- Normalize relative paths when `--project` is specified ([#9709](https://github.com/astral-sh/uv/pull/9709))
- Respect self-constraints on recursive extras ([#9714](https://github.com/astral-sh/uv/pull/9714))
- Respect user settings for tracing coloring ([#9733](https://github.com/astral-sh/uv/pull/9733))
- Retry on tar extraction errors ([#9753](https://github.com/astral-sh/uv/pull/9753))
- Add conflict markers to the lock file ([#9370](https://github.com/astral-sh/uv/pull/9370))
- De-duplicate resolution markers ([#9780](https://github.com/astral-sh/uv/pull/9780))
- Avoid 403 error hint for PyTorch URLs ([#9750](https://github.com/astral-sh/uv/pull/9750))
- Avoid treating non-existent `--find-links` as relative URLs ([#9720](https://github.com/astral-sh/uv/pull/9720))
- Omit Windows Store `python3.13.exe` et al ([#9679](https://github.com/astral-sh/uv/pull/9679))
- Replace executables with broken symlinks during `uv python install` ([#9706](https://github.com/astral-sh/uv/pull/9706))

### Documentation

- Fix build failure links ([#9740](https://github.com/astral-sh/uv/pull/9740))

## 0.5.7

### Enhancements

- Ignore dynamic version in source dist ([#9549](https://github.com/astral-sh/uv/pull/9549))
- Improve build frontend error handling ([#9611](https://github.com/astral-sh/uv/pull/9611))
- Un-hide `uv build --no-build-logs` option ([#9642](https://github.com/astral-sh/uv/pull/9642))
- Flag version mismatch between sdist and wheel during `uv build` ([#9633](https://github.com/astral-sh/uv/pull/9633))
- Improve message when updater receipt is for a different uv executable ([#9487](https://github.com/astral-sh/uv/pull/9487))
- Add environment variable to disable writing installer metadata files ([#8877](https://github.com/astral-sh/uv/pull/8877))
- Add managed downloads for the latest CPython releases: `3.9.21`, `3.10.16`, `3.11.11`, `3.12.8`, and `3.13.1` ([#9696](https://github.com/astral-sh/uv/pull/9696))

### Preview features

- Build backend: Add hint on import with preview disabled ([#9691](https://github.com/astral-sh/uv/pull/9691))
- Build backend: Add direct builds to the resolver and installer ([#9621](https://github.com/astral-sh/uv/pull/9621))
- Build backend: Add integration test for scripts ([#9635](https://github.com/astral-sh/uv/pull/9635))
- Build backend: Add template to `uv init` ([#9661](https://github.com/astral-sh/uv/pull/9661))
- Build backend: Add `--list` option ([#9610](https://github.com/astral-sh/uv/pull/9610))

### Bug fixes

- Create missing parent directories for output file of `uv export` / `uv pip compile` ([#9648](https://github.com/astral-sh/uv/pull/9648))
- Fix missing display of non-freethreaded Python 3.13 in `python list` ([#9669](https://github.com/astral-sh/uv/pull/9669))
- Implement `Ord` and `PartialOrd` without origin for `Requirement` ([#9624](https://github.com/astral-sh/uv/pull/9624))
- Include more sources to avoid lowest bound warning ([#9644](https://github.com/astral-sh/uv/pull/9644))
- Respect build tag priority in `uv.lock` ([#9677](https://github.com/astral-sh/uv/pull/9677))

### Documentation

- Add `build-essentials` note to build failures doc ([#9641](https://github.com/astral-sh/uv/pull/9641))
- Add entry-point for distroless image in GitLab documentation ([#9093](https://github.com/astral-sh/uv/pull/9093))
- Add documentation for `uv python pin` without a `REQUEST` argument ([#9631](https://github.com/astral-sh/uv/pull/9631))
- Add a link to `uv python pin` reference docs ([#9630](https://github.com/astral-sh/uv/pull/9630))

## 0.5.6

### Enhancements

- Add `--dry-run` to `uv pip uninstall` ([#9557](https://github.com/astral-sh/uv/pull/9557))
- Allow `--constraints` and `--overrides` in `uv tool install` ([#9547](https://github.com/astral-sh/uv/pull/9547))
- Display removed Python executables on uninstall ([#9459](https://github.com/astral-sh/uv/pull/9459))
- Warn when keyring has no password for `uv publish` ([#8827](https://github.com/astral-sh/uv/pull/8827))
- Add suggested action when `.python-version` pin is incompatible with the project ([#9590](https://github.com/astral-sh/uv/pull/9590))
- Improve error messages for mismatches in `tool.uv.sources` ([#9482](https://github.com/astral-sh/uv/pull/9482))
- Use constraints in trace rather than irrelevant `requires-python` ([#9529](https://github.com/astral-sh/uv/pull/9529))

### Preview features

- Add `uv python install --default` ([#8650](https://github.com/astral-sh/uv/pull/8650))
- Fix Python executable installation when multiple patch versions are requested ([#9607](https://github.com/astral-sh/uv/pull/9607))
- Build backend: Revamp `include` / `exclude` ([#9525](https://github.com/astral-sh/uv/pull/9525))
- Build backend: Add fast path  ([#9556](https://github.com/astral-sh/uv/pull/9556))
- Build backend: Add functions to collect file list ([#9602](https://github.com/astral-sh/uv/pull/9602))
- Build backend: Default excludes ([#9552](https://github.com/astral-sh/uv/pull/9552))
- Build backend: Refactoring before list ([#9558](https://github.com/astral-sh/uv/pull/9558))
- Build backend: Warn when visiting over 10k files  ([#9523](https://github.com/astral-sh/uv/pull/9523))

### Configuration

- Make `check-url` available in configuration files ([#9032](https://github.com/astral-sh/uv/pull/9032))

### Performance

- Avoid adding non-extra package with extra dependencies ([#9540](https://github.com/astral-sh/uv/pull/9540))
- Avoid cloning `String` in marker evaluation ([#9598](https://github.com/astral-sh/uv/pull/9598))

### Rust API

- `uv-pep508`: Add more methods for simplifying `extra`-related expressions ([#9469](https://github.com/astral-sh/uv/pull/9469))

### Bug fixes

- Allow `file:` URLs to include package names ([#9493](https://github.com/astral-sh/uv/pull/9493))
- Avoid using IDs across PubGrub states ([#9538](https://github.com/astral-sh/uv/pull/9538))
- Consistently enforce requested-vs.-built metadata when retrieving wheels ([#9484](https://github.com/astral-sh/uv/pull/9484))
- Do not show empty version specifier in `uv tool list` ([#9605](https://github.com/astral-sh/uv/pull/9605))
- Include Git member information when getting metadata from cache ([#9388](https://github.com/astral-sh/uv/pull/9388))
- Include base installation directory in uv run PATH ([#9585](https://github.com/astral-sh/uv/pull/9585))
- Insert backslash when appending to system drive ([#9488](https://github.com/astral-sh/uv/pull/9488))
- Normalize paths when lowering Git dependencies ([#9595](https://github.com/astral-sh/uv/pull/9595))
- Omit origin when comparing requirements ([#9570](https://github.com/astral-sh/uv/pull/9570))
- Override `manylinux_compatible` with `--python-platform` ([#9526](https://github.com/astral-sh/uv/pull/9526))
- Pass extra when evaluating lockfile markers ([#9539](https://github.com/astral-sh/uv/pull/9539))
- Propagate markers for recursive extras in resolver ([#9509](https://github.com/astral-sh/uv/pull/9509))
- Respect path dependencies within Git dependencies ([#9594](https://github.com/astral-sh/uv/pull/9594))
- Support recursive extras with marker in `pip compile -r pyproject.toml` ([#9535](https://github.com/astral-sh/uv/pull/9535))
- Don't emit unpinned warning for proxy packages ([#9497](https://github.com/astral-sh/uv/pull/9497))
- Fix `--refresh-package` flag mentioned as `--refresh-dependency` ([#9486](https://github.com/astral-sh/uv/pull/9486))
- Handle Windows AV/EDR file locks during script installations ([#9543](https://github.com/astral-sh/uv/pull/9543))
- Re-enable conflicting extra/group tests and fix regression from #9540 ([#9582](https://github.com/astral-sh/uv/pull/9582))

### Documentation

- Add missing word to docs for `run.md` ([#9527](https://github.com/astral-sh/uv/pull/9527))
- Add policies reference section and license document ([#9367](https://github.com/astral-sh/uv/pull/9367))
- Fix typo in entry point docs ([#9491](https://github.com/astral-sh/uv/pull/9491))
- Fix up version in prior uninstall instructions ([#9485](https://github.com/astral-sh/uv/pull/9485))
- Mention `uv pip` behavior in build system note ([#9586](https://github.com/astral-sh/uv/pull/9586))
- Update build failures document ([#9584](https://github.com/astral-sh/uv/pull/9584))
- Correct wording for multiple sources section ([#9504](https://github.com/astral-sh/uv/pull/9504))

## 0.5.5

### Enhancements

- Add aliases for build backend requests ([#9294](https://github.com/astral-sh/uv/pull/9294))
- Avoid displaying empty paths ([#9312](https://github.com/astral-sh/uv/pull/9312))
- Allow constraints in `uv tool upgrade` ([#9375](https://github.com/astral-sh/uv/pull/9375))
- Remove conflict between `--no-sync` and `--frozen` in `uv run` ([#9400](https://github.com/astral-sh/uv/pull/9400))
- Respect dependency sources in overrides and constraints ([#9455](https://github.com/astral-sh/uv/pull/9455))
- Show an interpreter-focused message for `--target` and `--prefix` ([#9373](https://github.com/astral-sh/uv/pull/9373))
- Add `--no-extra` flag and setting ([#9387](https://github.com/astral-sh/uv/pull/9387))
- Add `uv export --prune` ([#9389](https://github.com/astral-sh/uv/pull/9389))
- Add dedicated error message for musl install attempts ([#9430](https://github.com/astral-sh/uv/pull/9430))
- Add various grammar changes to conflict error messages ([#9369](https://github.com/astral-sh/uv/pull/9369))
- Annotate default groups in conflict error messages ([#9368](https://github.com/astral-sh/uv/pull/9368))
- Report marker diagnostics during parsing, rather than evaluation ([#9338](https://github.com/astral-sh/uv/pull/9338))
- Use consistent formatting for build system errors ([#9340](https://github.com/astral-sh/uv/pull/9340))
- Use rich diagnostics for build failures ([#9335](https://github.com/astral-sh/uv/pull/9335))

### Preview features

- Improve build backend excludes ([#9281](https://github.com/astral-sh/uv/pull/9281))
- Include PEP 639 `license-files` metadata during `uv publish` ([#9442](https://github.com/astral-sh/uv/pull/9442))

### Performance

- Initialize rayon lazily ([#9435](https://github.com/astral-sh/uv/pull/9435))
- Migrate to PubGrub's arena for package names ([#9448](https://github.com/astral-sh/uv/pull/9448))

### Bug fixes

- Allow dependency groups to include the containing package ([#9385](https://github.com/astral-sh/uv/pull/9385))
- Allow syncing to empty virtual environment directories ([#9427](https://github.com/astral-sh/uv/pull/9427))
- Allow system Python discovery with `--target` and `--prefix` ([#9371](https://github.com/astral-sh/uv/pull/9371))
- Don't warn when `--output-file` is empty ([#9417](https://github.com/astral-sh/uv/pull/9417))
- Fix Python interpreter discovery on non-glibc hosts ([#9005](https://github.com/astral-sh/uv/pull/9005))
- Fix `tool.uv.dependency-metadata.[].version` schema ([#9468](https://github.com/astral-sh/uv/pull/9468))
- Only respect preferences across the same indexes ([#9302](https://github.com/astral-sh/uv/pull/9302))
- Re-compile when `--compile` is passed to an install operation ([#9378](https://github.com/astral-sh/uv/pull/9378))
- Remove `--upgrade`, `--no-upgrade`, and `--upgrade-package` from `uv tool upgrade` ([#9318](https://github.com/astral-sh/uv/pull/9318))
- Remove dev dependencies in `--all-groups --no-dev` ([#9300](https://github.com/astral-sh/uv/pull/9300))
- Surface extras and group conflicts in `uv export` ([#9365](https://github.com/astral-sh/uv/pull/9365))
- Treat deprecated aliases as equivalent in marker algebra ([#9342](https://github.com/astral-sh/uv/pull/9342))
- Treat less compatible tags as lower priority in resolver ([#9339](https://github.com/astral-sh/uv/pull/9339))

### Documentation

- Avoid referencing `scikit-build` (instead of `scikit-build-core`) ([#9320](https://github.com/astral-sh/uv/pull/9320))
- Expand entry points documentation ([#9329](https://github.com/astral-sh/uv/pull/9329))
- Fix example `pyproject.toml` in project concept documentation ([#9298](https://github.com/astral-sh/uv/pull/9298))
- Fix header level of "Conflicting dependencies" page ([#9330](https://github.com/astral-sh/uv/pull/9330))
- Touch-up the extension module guide ([#9293](https://github.com/astral-sh/uv/pull/9293))
- Update the dependencies documentation ([#9359](https://github.com/astral-sh/uv/pull/9359))
- Reference `--no-progress` option in related environment variable ([#9357](https://github.com/astral-sh/uv/pull/9357))

## 0.5.4

### Enhancements

- Accept either singular or plural values for CLI requirements ([#9196](https://github.com/astral-sh/uv/pull/9196))
- Add `--all-groups` to `uv sync`, `uv run`, `uv export`, and `uv tree` ([#8892](https://github.com/astral-sh/uv/pull/8892))
- Add a progress bar to `uv tree --outdated` and `uv pip list --outdated` ([#9284](https://github.com/astral-sh/uv/pull/9284))
- Add retries for Python downloads ([#9274](https://github.com/astral-sh/uv/pull/9274))
- Use exponential backoff for publish retries ([#9276](https://github.com/astral-sh/uv/pull/9276))
- Add manylinux target triples up to glibc 2.40 ([#9234](https://github.com/astral-sh/uv/pull/9234))

### Performance

- Parallelize network requests in `uv tree --outdated` ([#9280](https://github.com/astral-sh/uv/pull/9280))
- Use `zlib-rs` on all platforms ([#9264](https://github.com/astral-sh/uv/pull/9264))

### Bug fixes

- Avoid validating extra and group sources in `build-system.requires` ([#9273](https://github.com/astral-sh/uv/pull/9273))
- Catch retries with wrapped `reqwest` errors ([#9253](https://github.com/astral-sh/uv/pull/9253))
- Sort hashes in `uv export` output ([#9237](https://github.com/astral-sh/uv/pull/9237))
- Strip `--index` and `--default-index` from command header ([#9288](https://github.com/astral-sh/uv/pull/9288))

### Documentation

- Add breadcrumbs to the documentation ([#9242](https://github.com/astral-sh/uv/pull/9242))
- Add minimum version to PyTorch guide ([#9247](https://github.com/astral-sh/uv/pull/9247))
- Add support for anchor redirects with client-side js ([#9212](https://github.com/astral-sh/uv/pull/9212))
- Improve content on project configuration ([#9235](https://github.com/astral-sh/uv/pull/9235))
- Improve the project creation documentation ([#9236](https://github.com/astral-sh/uv/pull/9236))
- Move the integration guides into the "Guides" section as a collapsed group ([#9245](https://github.com/astral-sh/uv/pull/9245))
- Reorganize the project concept documentation ([#9121](https://github.com/astral-sh/uv/pull/9121))
- Use the full screen height for the main content to stabilize the nav ([#9153](https://github.com/astral-sh/uv/pull/9153))

### Error messages

- Add dedicated warning for empty stdin ([#9256](https://github.com/astral-sh/uv/pull/9256))

## 0.5.3

This release includes support for conflicting optional dependencies and dependency groups in the uv resolver, including the ability to specify dependency sources (like index assignment) on a per-extra or per-group basis.

For example, you can now select CPU-only vs. GPU-enabled PyTorch builds at runtime by defining conflicting extras in a `pyproject.toml`, and assigning different extras to different PyTorch indexes:

```toml
[project]
name = "project"
version = "0.1.0"
requires-python = ">=3.12.0"

[project.optional-dependencies]
# Include `torch` whenever `--extra cpu` or `--extra gpu` is provided.
cpu = ["torch>=2.5.1"]
gpu = ["torch>=2.5.1"]

[tool.uv]
# But allow `cpu` and `gpu` to choose conflicting versions of `torch`.
conflicts = [[{ extra = "cpu" }, { extra = "gpu" }]]

[tool.uv.sources]
torch = [
  # With `--extra cpu`, pull PyTorch from the CPU-only index.
  { index = "pytorch-cpu", extra = "cpu", marker = "platform_system != 'Darwin'" },
  # With `--extra gpu`, pull PyTorch from the GPU-enabled index.
  { index = "pytorch-gpu", extra = "gpu" },
]

[[tool.uv.index]]
name = "pytorch-cpu"
url = "https://download.pytorch.org/whl/cpu"
explicit = true

[[tool.uv.index]]
name = "pytorch-gpu"
url = "https://download.pytorch.org/whl/cu124"
explicit = true
```

See the [PyTorch](https://docs.astral.sh/uv/guides/integration/pytorch/) documentation for more.

### Enhancements

- Allow conflicting extras in explicit index assignments ([#9160](https://github.com/astral-sh/uv/pull/9160))
- Support overrides and constraints in PEP 723 scripts ([#9162](https://github.com/astral-sh/uv/pull/9162))
- Update `uv tool install --force` to imply `--reinstall-package <name>` ([#9074](https://github.com/astral-sh/uv/pull/9074))
- Turn `--verify-hashes` on by default ([#9170](https://github.com/astral-sh/uv/pull/9170))

### Performance

- Enable `zlib-rs` on all platforms ([#9202](https://github.com/astral-sh/uv/pull/9202))

### Bug fixes

- Allow apostrophe in virtual environment name ([#8984](https://github.com/astral-sh/uv/pull/8984))
- Automatically retry body errors when processing response ([#9213](https://github.com/astral-sh/uv/pull/9213))
- Detect nested workspace inside the current workspace and members with identical names ([#9094](https://github.com/astral-sh/uv/pull/9094))
- Only install the specified project with `--frozen --package` in legacy non-`[project]` workspaces ([#9215](https://github.com/astral-sh/uv/pull/9215))
- Respect `[[tool.uv.index]]` in PEP 723 scripts ([#9208](https://github.com/astral-sh/uv/pull/9208))
- Show derivation markers for resolutions with project name ([#9136](https://github.com/astral-sh/uv/pull/9136))
- Sort distributions when computing hash ([#9185](https://github.com/astral-sh/uv/pull/9185))
- Include trampolines in source distributions on Windows ([#9172](https://github.com/astral-sh/uv/pull/9172))

### Documentation

- Add `--index <name>=<url>` syntax to index documentation ([#9139](https://github.com/astral-sh/uv/pull/9139))
- Add documentation for using uv with PyTorch ([#9210](https://github.com/astral-sh/uv/pull/9210))

### Error messages

- Add a dedicated error for `include = "dev"` with `tool.uv.dev-dependencies` ([#9173](https://github.com/astral-sh/uv/pull/9173))
- Avoid showing disjoint marker error with `true` ([#9169](https://github.com/astral-sh/uv/pull/9169))
- Improve error message when `git` is not found ([#9206](https://github.com/astral-sh/uv/pull/9206))
- Include extras and dependency groups in derivation chains ([#9113](https://github.com/astral-sh/uv/pull/9113))
- Include version constraints in derivation chains ([#9112](https://github.com/astral-sh/uv/pull/9112))

## 0.5.2

### Enhancements

- Hide `--no-system` from `uv pip tree` CLI ([#9040](https://github.com/astral-sh/uv/pull/9040))
- Allow configuration of Python and PyPy install mirrors in `uv.toml` ([#8695](https://github.com/astral-sh/uv/pull/8695))
- Allow passing Python download mirrors to `uv python install` ([#8695](https://github.com/astral-sh/uv/pull/8695))
- Add support for specifying conflicting extras and dependency groups ([#8976](https://github.com/astral-sh/uv/pull/8976), [#9096](https://github.com/astral-sh/uv/pull/9096))
- Consistent colon usage in build failure errors ([#8994](https://github.com/astral-sh/uv/pull/8994))
- Show full derivation chain when encountering build failures ([#9108](https://github.com/astral-sh/uv/pull/9108))
- Show link we failed on parsing index pages ([#9118](https://github.com/astral-sh/uv/pull/9118))
- Remove duplicate log when searching for interpreters ([#9092](https://github.com/astral-sh/uv/pull/9092))
- Update uv development status classifier to "Stable" on PyPI ([#8943](https://github.com/astral-sh/uv/pull/8943))
- Use rich diagnostic formatting for early build failures ([#9041](https://github.com/astral-sh/uv/pull/9041))
- Use rich diagnostic formatting for install failures ([#9043](https://github.com/astral-sh/uv/pull/9043))

### Performance

- Avoid retraversing filesystem when testing exact glob matches ([#9022](https://github.com/astral-sh/uv/pull/9022))

### Bug fixes

- Allow `--no-build` to validate lock ([#9024](https://github.com/astral-sh/uv/pull/9024))
- Allow default indexes to be marked as explicit ([#8990](https://github.com/astral-sh/uv/pull/8990))
- Avoid creating `.venv` in `uv add --frozen` and `uv add --no-sync` ([#8980](https://github.com/astral-sh/uv/pull/8980))
- Avoid duplicating first-entry comments in `uv add` ([#9109](https://github.com/astral-sh/uv/pull/9109))
- Defer reporting of build failures in resolver ([#9098](https://github.com/astral-sh/uv/pull/9098))
- Fix references to `--resolution-strategy` in error message output ([#8971](https://github.com/astral-sh/uv/pull/8971))
- Ignore virtual environments in parent directories when choosing Python version for new projects ([#9075](https://github.com/astral-sh/uv/pull/9075))
- Forward SIGTERM to child processes in `uv run` ([#8933](https://github.com/astral-sh/uv/pull/8933))
- Prefer Python executable names that match the request over default names ([#9066](https://github.com/astral-sh/uv/pull/9066))
- Prefer compatible to incompatible distributions when packages exist on multiple indexes ([#8961](https://github.com/astral-sh/uv/pull/8961))
- Publish: Ignore non-matching files ([#8986](https://github.com/astral-sh/uv/pull/8986))
- Revert `uv.lock` changes when `uv add` fails ([#9030](https://github.com/astral-sh/uv/pull/9030))
- Show file extensions on available commands when not `.exe` ([#9099](https://github.com/astral-sh/uv/pull/9099))
- Sort by name, then specifiers in `uv add` ([#9097](https://github.com/astral-sh/uv/pull/9097))
- Split after specifiers in `--with` requirements ([#9089](https://github.com/astral-sh/uv/pull/9089))
- Support multiple extras in universal pip compile output ([#8960](https://github.com/astral-sh/uv/pull/8960))

### Preview features

- Build backend: Add tests for source tree -> source dist -> wheel conversions ([#9091](https://github.com/astral-sh/uv/pull/9091))
- Build backend: Switch to custom `glob-walkdir` implementation ([#9013](https://github.com/astral-sh/uv/pull/9013))
- Build backend: Add minimal wheel settings ([#9085](https://github.com/astral-sh/uv/pull/9085))

### Documentation

- Add wget instructions for systems without curl ([#8630](https://github.com/astral-sh/uv/pull/8630))
- Fix `.env` file example in docs ([#9064](https://github.com/astral-sh/uv/pull/9064))
- Fix reference to `--resolution` in docs ([#8968](https://github.com/astral-sh/uv/pull/8968))
- Fix typo in GitLab integration docs ([#9047](https://github.com/astral-sh/uv/pull/9047))
- Update format of environment variable reference ([#9018](https://github.com/astral-sh/uv/pull/9018))
- Use Python syntax for `value_type` consistently ([#9017](https://github.com/astral-sh/uv/pull/9017))
- Use `[[index]]` API in configuration example ([#9065](https://github.com/astral-sh/uv/pull/9065))
- Mention how to use extras ([#8972](https://github.com/astral-sh/uv/pull/8972))
- Add some words about specifying conflicting extras/groups ([#9120](https://github.com/astral-sh/uv/pull/9120))

## 0.5.1

### Enhancements

- Allow installation of manylinux wheels on `riscv64` ([#8934](https://github.com/astral-sh/uv/pull/8934))

### Bug fixes

- Build source distributions at top-level of cache ([#8905](https://github.com/astral-sh/uv/pull/8905))
- Allow non-registry dependencies in `uv pip list --outdated` ([#8939](https://github.com/astral-sh/uv/pull/8939))
- Compute superset of existing and required hashes when healing cache ([#8955](https://github.com/astral-sh/uv/pull/8955))
- Enable uv to replace and delete itself on Windows ([#8914](https://github.com/astral-sh/uv/pull/8914))
- Remove source distribution filename from cache ([#8907](https://github.com/astral-sh/uv/pull/8907))
- Respect `--index-url` in `uv pip list` ([#8942](https://github.com/astral-sh/uv/pull/8942))
- Respect comma-separated extras in `--with` ([#8946](https://github.com/astral-sh/uv/pull/8946))

### Documentation

- Add uninstall note for previous versions ([#8937](https://github.com/astral-sh/uv/pull/8937))
- Remove some missed references to `~/.cargo/bin` ([#8936](https://github.com/astral-sh/uv/pull/8936))
- Split README's install code block into 3 ([#8853](https://github.com/astral-sh/uv/pull/8853))

## 0.5.0

Since the launch of Python version, project, and tool management capabilities back in August, we've seen extraordinary adoption of uv. We've been iterating rapidly: adding new features, fixing bugs, and improving the user experience. Despite moving quickly, stability and compatibility have been a major focus — we've made thirty releases since our last breaking change. Consequently, we've accumulated various changes that improve correctness and user experience, but could break some workflows. This release contains those changes; many have been marked as breaking out of an abundance of caution. We expect most users to be able to upgrade without making changes.

### Breaking

- **Use base executable to set virtualenv Python path** ([#8481](https://github.com/astral-sh/uv/pull/8481))
  
  Previously, uv canonicalized the path to the Python executable when setting the Python path in created virtual environments. This behavior had several undesirable effects: it would bypass stabilized version directories (as constructed by Homebrew) and it was not consistent with the Python standard library's behavior. Now, uv uses the `sys._base_executable` path.
- **Use XDG (i.e. `~/.local/bin`) instead of the Cargo home directory in the installer** ([#8420](https://github.com/astral-sh/uv/pull/8420))
  
  Previously, uv's installer used `$CARGO_HOME` or `~/.cargo/bin` for its target install directory. It's been a longstanding complaint that uv uses this directory, as there's no relationship to Cargo. Now, uv will be installed into `$XDG_BIN_HOME`, `$XDG_DATA_HOME/../bin`, or `~/.local/bin` (in that order). Note that `$UV_INSTALL_DIR` can always be used to override the target directory.
- **Discover and respect `.python-version` files in parent directories** ([#6370](https://github.com/astral-sh/uv/pull/6370))
  
  Previously, uv only read `.python-version` files from the working directory. Now, uv will check parent directories for `.python-version` files; however uv will not search for `.python-version` files beyond project boundaries. The new behavior is better aligned with that of `pyenv` and Rye.
- **Error when disallowed settings are defined in `uv.toml`** ([#8550](https://github.com/astral-sh/uv/pull/8550))
  
  Some settings can only be defined in the `pyproject.toml`. Previously, uv would ignore these settings when present in the `uv.toml`. Now, uv will error to avoid confusion about why the settings are not respected.
- **Implement PEP 440-compliant local version semantics** ([#8797](https://github.com/astral-sh/uv/pull/8797))
  
  Previously, uv's implementation of local versions (e.g. `2.0+cpu`) was not compliant with the specification due to the technical complexity of implementing the local version semantics in the PubGrub algorithm. Thanks to the work of @ericmarkmartin, uv now has a spec-compliant implementation. Namely, uv will now allow a request for `torch==2.1.0` to install `torch@2.1.0+cpu` regardless of whether `torch@2.1.0` (without a local tag) actually exists.
- **Treat the base Conda environment as a system environment** ([#7691](https://github.com/astral-sh/uv/pull/7691))
  
  Previously, uv would not distinguish between the base and other Conda environments. Now, uv uses `CONDA_DEFAULT_ENV` and the names `base` and `default` to determine if an environment active via `CONDA_PREFIX` is the base environment. If the base environment is active, the `--system` flag must be used to mutate it.
- **Do not allow pre-releases when the `!=` operator is used** ([#7974](https://github.com/astral-sh/uv/pull/7974))
  
  Previously, uv would use the presence of a pre-release specifier in a version specifier as an opt-in to allow pre-release versions during resolution. The new behavior does not allow pre-releases when an inequals operator is used, e.g., `!= 2.0a1`.
- **Prefer `USERPROFILE` over `FOLDERID_Profile` when selecting a home directory on Windows** ([#8048](https://github.com/astral-sh/uv/pull/8048))
  
  This change is a side-effect of switching from the `directories` crate to `etcetera` for determining canonical system paths. If `USERPROFILE` is not set, the behavior will be unchanged.
- **Improve interactions between color environment variables and CLI options** ([#8215](https://github.com/astral-sh/uv/pull/8215))
  
  Previously, uv would respect the `FORCE_COLOR` and `NO_COLOR` environment variables over the `--color` flag. Now, when the `--color` flag is explicitly provided, uv will respect it over the environment variables.
- **Make `allow-insecure-host` a global option** ([#8476](https://github.com/astral-sh/uv/pull/8476))
  
  Previously, this option was only available in some parts of uv. Now, `--allow-insecure-host` can be provided to any command. For consistency, the `allow-insecure-host` setting has been removed from the `[tool.uv.pip]` configuration in favor of `[tool.uv]`.
- **Only write `.python-version` files during `uv init` for workspace members if the version differs** ([#8897](https://github.com/astral-sh/uv/pull/8897))
  
  Previously, uv would create a `.python-version` file for workspace members during `uv init`. Now, uv will only do so if the version differs from the `.python-version` file in the workspace root since uv will respect `.python-version` files in parent directories.

### Enhancements

- Add `uv tree --outdated` ([#8893](https://github.com/astral-sh/uv/pull/8893))
- Add armv8l alias for armv7l to support arm 32-bit compatibility mode ([#8881](https://github.com/astral-sh/uv/pull/8881))
- Add support for `pip list --outdated` ([#8872](https://github.com/astral-sh/uv/pull/8872))
- Allow semicolons directly after direct URLs ([#8836](https://github.com/astral-sh/uv/pull/8836))
- Enable support for arbitrary git transports ([#8769](https://github.com/astral-sh/uv/pull/8769))
- Improve Python discovery source messages ([#8890](https://github.com/astral-sh/uv/pull/8890))
- Show dedicated error for trailing `;` on URL and path requirements ([#8835](https://github.com/astral-sh/uv/pull/8835))
- Add progress bar for `uv cache clean` ([#8857](https://github.com/astral-sh/uv/pull/8857))
- Warn on failure to query system configuration file ([#8829](https://github.com/astral-sh/uv/pull/8829))

### Preview features

- Add support for building basic source distributions with the experimental uv build backend ([#8886](https://github.com/astral-sh/uv/pull/8886))

### Bug fixes

- Respect dynamic version updates in `uv lock` ([#8867](https://github.com/astral-sh/uv/pull/8867))
- Respect fork markers in `--resolution-mode=lowest-direct` ([#8839](https://github.com/astral-sh/uv/pull/8839))

### Documentation

- Add further examples of git+https support ([#8841](https://github.com/astral-sh/uv/pull/8841))
- Add installer variables to environment reference ([#8874](https://github.com/astral-sh/uv/pull/8874))
- Add note on private classifier ([#8783](https://github.com/astral-sh/uv/pull/8783))
- Update pip-and-uv strictness example ([#8822](https://github.com/astral-sh/uv/pull/8822))
- Fix `uv python install` docs to use an existing PyPy version ([#8845](https://github.com/astral-sh/uv/pull/8845))
- Document how to mimic `--verbose` with `RUST_LOG` ([#8858](https://github.com/astral-sh/uv/pull/8858))

## 0.4.30

### Enhancements

- Add support for `.env` and custom env files in `uv run` ([#8811](https://github.com/astral-sh/uv/pull/8811))
- Add support for `--all-packages` in `uv run`, `uv sync`, and `uv export` ([#8742](https://github.com/astral-sh/uv/pull/8742), [#8741](https://github.com/astral-sh/uv/pull/8741), [#8739](https://github.com/astral-sh/uv/pull/8739))
- Allow use of `--frozen` with `--all-packages` in `uv sync` and `uv export` ([#8760](https://github.com/astral-sh/uv/pull/8760))
- Show full error chain on tool upgrade failures ([#8753](https://github.com/astral-sh/uv/pull/8753))
- Add `--check-url` to `uv publish` to check for existing distributions during upload ([#8531](https://github.com/astral-sh/uv/pull/8531))
- Suggest using `--check-url` when `--skip-existing` is used ([#8803](https://github.com/astral-sh/uv/pull/8803))

### Bug fixes

- Allow incompatible `requires-python` for source distributions with static metadata ([#8768](https://github.com/astral-sh/uv/pull/8768))
- Allow managed downloads with `--python-preference system` ([#8808](https://github.com/astral-sh/uv/pull/8808))
- Avoid error for `--group` defined in non-root workspace member ([#8734](https://github.com/astral-sh/uv/pull/8734))
- Avoid showing dependency group annotations on workspace members in tree ([#8730](https://github.com/astral-sh/uv/pull/8730))
- Do not error when the Python bin directory is missing on `uv python uninstall` ([#8725](https://github.com/astral-sh/uv/pull/8725))
- Include member groups when locking workspace ([#8736](https://github.com/astral-sh/uv/pull/8736))
- Fix bug where `python_version < '0'` could appear in a final resolution ([#8759](https://github.com/astral-sh/uv/pull/8759))
- Sanitize filenames during zip extraction ([#8732](https://github.com/astral-sh/uv/pull/8732))
- Switch to RFC 9110 compatible format for exclude newer requests ([#8752](https://github.com/astral-sh/uv/pull/8752))

### Preview features

- Add support for installing versioned Python executables on Windows ([#8663](https://github.com/astral-sh/uv/pull/8663))
- Improve interactions with existing Python executables during install ([#8733](https://github.com/astral-sh/uv/pull/8733))

### Rust API

- Extend `BaseClient` to accept extra middleware ([#8807](https://github.com/astral-sh/uv/pull/8807))
- Add `From` for `FlatDistributions` struct ([#8800](https://github.com/astral-sh/uv/pull/8800))

### Documentation

- Fix environment variable name in providing credentials section ([#8740](https://github.com/astral-sh/uv/pull/8740))
- Fix `add httpx` example with real git branch ([#8756](https://github.com/astral-sh/uv/pull/8756))
- Fix indentation in `projects.md` ([#8772](https://github.com/astral-sh/uv/pull/8772))
- Fix link to publish guide in `README` ([#8720](https://github.com/astral-sh/uv/pull/8720))
- Generate environment variables documentation from code ([#8493](https://github.com/astral-sh/uv/pull/8493))
- Improve and fix some documents ([#8749](https://github.com/astral-sh/uv/pull/8749))
- Improve environment variables document ([#8777](https://github.com/astral-sh/uv/pull/8777))

## 0.4.29

### Enhancements

- Sort errors during display in `uv python install` ([#8684](https://github.com/astral-sh/uv/pull/8684))
- Update resolver to use disjointness checks instead of marker equality ([#8661](https://github.com/astral-sh/uv/pull/8661))
- Add `riscv64` to supported Python platform tags ([#8660](https://github.com/astral-sh/uv/pull/8660))

### Bug fixes

- Fix hard and soft float libc detection for managed Python distributions on ARM ([#8498](https://github.com/astral-sh/uv/pull/8498))
- Handle cycles in `uv pip tree` ([#8689](https://github.com/astral-sh/uv/pull/8689))
- Respect dependency group markers in `uv export` ([#8659](https://github.com/astral-sh/uv/pull/8659))
- Support transitive dependencies in Git workspaces ([#8665](https://github.com/astral-sh/uv/pull/8665))
- Use portable paths for subdirectories in lock URLs ([#8707](https://github.com/astral-sh/uv/pull/8707))
- Update `uv init --virtual` to imply `--no-package` ([#8595](https://github.com/astral-sh/uv/pull/8595))

### Preview

- Install versioned Python executables into the bin directory during `uv python install` (Unix only) ([#8458](https://github.com/astral-sh/uv/pull/8458))

### Documentation

- Clarify relationship between specifiers and `requires-python` range ([#8688](https://github.com/astral-sh/uv/pull/8688))
- Fix broken link in docs ([#8552](https://github.com/astral-sh/uv/pull/8552))
- Fix outdated documentation on `Requires-Python` ([#8679](https://github.com/astral-sh/uv/pull/8679))
- Add Google Artifact Registry index authentication guide ([#8579](https://github.com/astral-sh/uv/pull/8579))

## 0.4.28

### Enhancements

- Add support for requesting free-threaded builds via `+freethreaded` ([#8645](https://github.com/astral-sh/uv/pull/8645))
- Improve trusted publishing error messages ([#8633](https://github.com/astral-sh/uv/pull/8633))
- Remove unneeded `return` from Maturin project template ([#8604](https://github.com/astral-sh/uv/pull/8604))
- Skip Python interpreter discovery for `uv export` ([#8638](https://github.com/astral-sh/uv/pull/8638))
- Hint about missing trusted publishing permission ([#8632](https://github.com/astral-sh/uv/pull/8632))

### Configuration

- Add environment variable to disable progress output ([#8600](https://github.com/astral-sh/uv/pull/8600))

### Bug fixes

- Fork when minimum Python version increases ([#8628](https://github.com/astral-sh/uv/pull/8628))
- Ignore empty groups when validating lock ([#8598](https://github.com/astral-sh/uv/pull/8598))
- Remove duplicate word in error message ([#8589](https://github.com/astral-sh/uv/pull/8589))
- Support cyclic dependencies in `uv tree` ([#8564](https://github.com/astral-sh/uv/pull/8564))
- Update `uv init` to imply `--package` when using `--build-backend` ([#8593](https://github.com/astral-sh/uv/pull/8593))
- Restore use of `dev-dependencies` and `requires-dev` for lockfile compatibility ([#8599](https://github.com/astral-sh/uv/pull/8599))

### Documentation

- Clarify `requires-python` requirement for dependencies ([#8619](https://github.com/astral-sh/uv/pull/8619))
- Update CLI documentation for `--cache-dir` ([#8627](https://github.com/astral-sh/uv/pull/8627))

## 0.4.27

This release includes support for the `[dependency-groups]` table as recently standardized in [PEP 735](https://peps.python.org/pep-0735/). The table allows for declaration of optional dependency groups that are not published as part of the package metadata, unlike `[project.optional-dependencies]`. There are new `--group`, `--only-group`, and `--no-group` options throughout the uv interface.

Previously, uv used a single `tool.uv.dev-dependencies` list for declaration of development dependencies. Now, uv supports declaring development dependencies in a standardized format and allows splitting development dependencies into multiple groups.

For compatibility, and to simplify usage for people that do not need multiple groups, uv special-cases the group named `dev`. The `dev` group is equivalent to `tool.uv.dev-dependencies`. The contents of `tool.uv.dev-dependencies` will merged into the `dev` group in uv's resolver. The `--dev`, `--only-dev`, and `--no-dev` flags remain as aliases for the corresponding `--group` options. Support for `tool.uv.dev-dependencies` remains in this release, but will display warnings in a future release.

uv syncs the `dev` group by default — this matches the existing behavior for `tool.uv.dev-dependencies`. The default groups can be changed with the `tool.uv.default-groups` setting.

Thank you to Stephen Rosen who authored PEP 735.

### Enhancements

- Support for PEP 735 ([#8272](https://github.com/astral-sh/uv/pull/8272))
- Add support for `--dry-run` mode in `uv lock` ([#7783](https://github.com/astral-sh/uv/pull/7783))
- Don't allow non-string email in authors ([#8520](https://github.com/astral-sh/uv/pull/8520))
- Enforce lockfile schema versions ([#8509](https://github.com/astral-sh/uv/pull/8509))

### Bug fixes

- Always attach URL to network errors ([#8444](https://github.com/astral-sh/uv/pull/8444))
- Fix dangling non-platform dependencies in `uv tree` ([#8532](https://github.com/astral-sh/uv/pull/8532))
- Prefer `lto` over `debug` free-threaded managed Python builds ([#8515](https://github.com/astral-sh/uv/pull/8515))

### Documentation

- Add `tool.uv.sources` to the "Settings" reference ([#8543](https://github.com/astral-sh/uv/pull/8543))
- Add reference to `uv build` and `uv publish` in the landing pages ([#8542](https://github.com/astral-sh/uv/pull/8542))
- Avoid duplicate `[tool.uv]` header in TOML examples ([#8545](https://github.com/astral-sh/uv/pull/8545))
- Document `.netrc` environment variable and path ([#8511](https://github.com/astral-sh/uv/pull/8511))
- Fix `.netrc` typo in authentication docs ([#8521](https://github.com/astral-sh/uv/pull/8521))
- Fix heading level of "Script support" on docs landing page ([#8544](https://github.com/astral-sh/uv/pull/8544))
- Move the installation configuration docs to a separate page ([#8546](https://github.com/astral-sh/uv/pull/8546))
- Update docs for `--publish-url` to avoid duplication. ([#8561](https://github.com/astral-sh/uv/pull/8561))
- Fix typo ([#8554](https://github.com/astral-sh/uv/pull/8554))
- Fix typo in description of `--strict` flag ([#8513](https://github.com/astral-sh/uv/pull/8513))

## 0.4.26

### Enhancements

- Allow static dependency metadata entries for direct URL requirements ([#7846](https://github.com/astral-sh/uv/pull/7846))
- Use reinstall report formatting for `uv python install --reinstall` ([#8487](https://github.com/astral-sh/uv/pull/8487))
- Add support for system-level `uv.toml` configuration ([#7851](https://github.com/astral-sh/uv/pull/7851))

### Bug fixes

- Apply `requires-python` narrowing with upper bounds ([#8403](https://github.com/astral-sh/uv/pull/8403))
- Avoid rewriting `[[tool.uv.index]]` entries when credentials are provided ([#8502](https://github.com/astral-sh/uv/pull/8502))
- Fix `uv add` comment handling for empty arrays ([#8504](https://github.com/astral-sh/uv/pull/8504))
- Replace dashes with underscores in index credential variables ([#8452](https://github.com/astral-sh/uv/pull/8452))
- Respect `--allow-insecure-host` in `uv publish` ([#8440](https://github.com/astral-sh/uv/pull/8440))
- Allow arbitrary `--package` includes in `uv tree` ([#8507](https://github.com/astral-sh/uv/pull/8507))
- Remove existing Python install after successful download in `uv python install` ([#8485](https://github.com/astral-sh/uv/pull/8485))

### Documentation

- Add docs example for URLs with `[tool.uv.dependency-metadata]` ([#8484](https://github.com/astral-sh/uv/pull/8484))
- Add help page for build failures ([#8286](https://github.com/astral-sh/uv/pull/8286))
- Fix `cache-keys` typo in `tags = true` ([#8422](https://github.com/astral-sh/uv/pull/8422))
- Add documentation examples for manual branch, rev, and tag Git dependencies ([#8497](https://github.com/astral-sh/uv/pull/8497))

### Error messages

- Improve error message for cache info serialization ([#8500](https://github.com/astral-sh/uv/pull/8500))
- Suggest `--from` command when executable is available for `uvx` ([#8473](https://github.com/astral-sh/uv/pull/8473))
- Support `--with-editable` in `uv tool install` ([#8472](https://github.com/astral-sh/uv/pull/8472))

## 0.4.25

### Enhancements

- Add support for `uv pip show --files` ([#8369](https://github.com/astral-sh/uv/pull/8369))
- Don't prefetch unreachable packages ([#8246](https://github.com/astral-sh/uv/pull/8246))
- Remove `tool.uv.sources` table if it is empty ([#8365](https://github.com/astral-sh/uv/pull/8365))
- Modify cache versioning to support backwards compatibility ([#8386](https://github.com/astral-sh/uv/pull/8386))

### Configuration

- Add support for `UV_FROZEN` and `UV_LOCKED` ([#8340](https://github.com/astral-sh/uv/pull/8340))

### Bug fixes

- Allow dashes and underscores in custom index names ([#8339](https://github.com/astral-sh/uv/pull/8339))
- Avoid panic when Git dependencies are included in fork markers ([#8388](https://github.com/astral-sh/uv/pull/8388))
- Check existing source by normalized name before `uv add` and `uv remove` ([#8359](https://github.com/astral-sh/uv/pull/8359))
- Fix bug where username from authentication cache could be ignored ([#8345](https://github.com/astral-sh/uv/pull/8345))
- Fix to respect comments positioning in pyproject.toml on change ([#8384](https://github.com/astral-sh/uv/pull/8384))
- Redact index sources in `uv.lock` ([#8333](https://github.com/astral-sh/uv/pull/8333))
- Use correct indentation when project table contains open bracket comment ([#8387](https://github.com/astral-sh/uv/pull/8387))
- Only remove a source from `[tool.uv.sources]` if it is no long being referenced ([#8366](https://github.com/astral-sh/uv/pull/8366))
- Modify `uv pip list` and `uv tree` to print to stdout regardless of `--quiet` flag ([#8392](https://github.com/astral-sh/uv/pull/8392))

### Error messages

- Improve help message for missing `self update` invocations ([#8337](https://github.com/astral-sh/uv/pull/8337))
- Log `.netrc` parsing errors ([#8364](https://github.com/astral-sh/uv/pull/8364))
- Remove trailing newlines in error messages ([#8322](https://github.com/astral-sh/uv/pull/8322))
- Use a dedicated message for incompatible Python versions in wheel ABI tags ([#8363](https://github.com/astral-sh/uv/pull/8363))
- Remove commands available in the top-level from the suggested subcommand error ([#8316](https://github.com/astral-sh/uv/pull/8316))

### Release

- Run release builds for `macos-x86_64` on `macos-14` runners ([#8327](https://github.com/astral-sh/uv/pull/8327))

## 0.4.24

### Bug fixes

- Fix Python executable name in Windows free-threaded Python distributions ([#8310](https://github.com/astral-sh/uv/pull/8310))
- Redact index credentials from lockfile sources ([#8307](https://github.com/astral-sh/uv/pull/8307))
- Respect `UV_INDEX_` rather than `UV_HTTP_BASIC_` as documented ([#8306](https://github.com/astral-sh/uv/pull/8306))
- Improve sources deserialization errors ([#8308](https://github.com/astral-sh/uv/pull/8308))

### Documentation

- Correct pytorch-to-torch reference in docs ([#8291](https://github.com/astral-sh/uv/pull/8291))

## 0.4.23

This release introduces a revamped system for defining package indexes, as an alternative to the existing pip-style
`--index-url` and `--extra-index-url` configuration options.

You can now define named indexes in your `pyproject.toml` file using the `[[tool.uv.index]]` table:

```toml
[[tool.uv.index]]
name = "pytorch"
url = "https://download.pytorch.org/whl/cpu"
```

Packages can be pinned to a specific index via `tool.uv.sources`, to ensure that a given package is installed from the
correct index. For example, to ensure that `torch` is *always* installed from the `pytorch` index:

```toml
[tool.uv.sources]
torch = { index = "pytorch" }

[[tool.uv.index]]
name = "pytorch"
url = "https://download.pytorch.org/whl/cpu"
```

Indexes can also be marked as `explicit = true` to prevent packages from being installed from that index
unless explicitly pinned. For example, to ensure that `torch` is installed from the `pytorch` index, but all other
packages are installed from the default index:

```toml
[tool.uv.sources]
torch = { index = "pytorch" }

[[tool.uv.index]]
name = "pytorch"
url = "https://download.pytorch.org/whl/cpu"
explicit = true
```

To define an additional index outside a `pyproject.toml` file, use the `--index` command-line argument
(or the `UV_INDEX` environment variable); to replace the default index (PyPI), use the `--default-index` command-line
argument (or `UV_DEFAULT_INDEX`).

These changes are entirely backwards-compatible with the deprecated `--index-url` and `--extra-index-url` options,
which continue to work as before.

See the [Index](https://docs.astral.sh/uv/configuration/indexes/) documentation for more.

### Enhancements

- Add index URLs when provided via `uv add --index` or `--default-index` ([#7746](https://github.com/astral-sh/uv/pull/7746))
- Add support for named and explicit indexes ([#7481](https://github.com/astral-sh/uv/pull/7481))
- Add templates for popular build backends ([#7857](https://github.com/astral-sh/uv/pull/7857))
- Allow multiple pinned indexes in `tool.uv.sources` ([#7769](https://github.com/astral-sh/uv/pull/7769))
- Allow users to incorporate Git tags into dynamic cache keys ([#8259](https://github.com/astral-sh/uv/pull/8259))
- Pin named indexes in `uv add` ([#7747](https://github.com/astral-sh/uv/pull/7747))
- Respect named `--index` and `--default-index` values in `tool.uv.sources` ([#7910](https://github.com/astral-sh/uv/pull/7910))
- Update to latest PubGrub version ([#8245](https://github.com/astral-sh/uv/pull/8245))
- Enable environment variable authentication for named indexes ([#7741](https://github.com/astral-sh/uv/pull/7741))
- Avoid showing lower-bound warning outside of explicit lock and sync ([#8234](https://github.com/astral-sh/uv/pull/8234))
- Improve logging during lock errors ([#8258](https://github.com/astral-sh/uv/pull/8258))
- Improve styling of `requires-python` warnings ([#8240](https://github.com/astral-sh/uv/pull/8240))
- Show hint in resolution failure on `Forbidden` (`403`) or `Unauthorized` (`401`) ([#8264](https://github.com/astral-sh/uv/pull/8264))
- Update to latest `cargo-dist` version (includes new installer features) ([#8270](https://github.com/astral-sh/uv/pull/8270))
- Warn when patch version in `requires-python` is implicitly `0` ([#7959](https://github.com/astral-sh/uv/pull/7959))
- Add more context on client errors during range requests ([#8285](https://github.com/astral-sh/uv/pull/8285))

### Bug fixes

- Avoid writing duplicate index URLs with `--emit-index-url` ([#8226](https://github.com/astral-sh/uv/pull/8226))
- Fix error leading to out-of-bound panic in `uv-pep508` ([#8282](https://github.com/astral-sh/uv/pull/8282))
- Fix managed distributions of free-threaded Python on Windows ([#8268](https://github.com/astral-sh/uv/pull/8268))
- Fix selection of free-threaded interpreters during default Python discovery ([#8239](https://github.com/astral-sh/uv/pull/8239))
- Ignore sources in build requirements for non-source trees ([#8235](https://github.com/astral-sh/uv/pull/8235))
- Invalid cache when adding lower bound to lockfile ([#8230](https://github.com/astral-sh/uv/pull/8230))
- Respect index priority when storing credentials ([#8256](https://github.com/astral-sh/uv/pull/8256))
- Respect relative paths in `uv build` sources ([#8237](https://github.com/astral-sh/uv/pull/8237))
- Narrow what the pip3.<minor> logic drops from entry points. ([#8273](https://github.com/astral-sh/uv/pull/8273))

### Documentation

- Add some additional notes to `--index-url` docs ([#8267](https://github.com/astral-sh/uv/pull/8267))
- Add upgrade note to README ([#7937](https://github.com/astral-sh/uv/pull/7937))
- Remove note that "only a single source may be defined for each dependency" ([#8243](https://github.com/astral-sh/uv/pull/8243))

## 0.4.22

### Enhancements

- Respect `[tool.uv.sources]` in build requirements ([#7172](https://github.com/astral-sh/uv/pull/7172))

### Preview features

- Add a dedicated `uv publish` error message for missing usernames ([#8045](https://github.com/astral-sh/uv/pull/8045))
- Support interactive input in `uv publish` ([#8158](https://github.com/astral-sh/uv/pull/8158))
- Use raw filenames in `uv publish` ([#8204](https://github.com/astral-sh/uv/pull/8204))

### Performance

- Reuse the result of `which git` ([#8224](https://github.com/astral-sh/uv/pull/8224))

### Bug fixes

- Avoid environment check optimization for `uv pip install --exact` ([#8219](https://github.com/astral-sh/uv/pull/8219))
- Do not use free-threaded interpreters without a free-threaded request ([#8191](https://github.com/astral-sh/uv/pull/8191))
- Don't recommend `--prerelease=allow` during build requirement resolution errors ([#8192](https://github.com/astral-sh/uv/pull/8192))
- Prefer optimized builds for free-threaded Python downloads ([#8196](https://github.com/astral-sh/uv/pull/8196))
- Retain old `python-build-standalone` releases ([#8216](https://github.com/astral-sh/uv/pull/8216))
- Run `uv build` builds in the source distribution bucket ([#8220](https://github.com/astral-sh/uv/pull/8220))

## 0.4.21

### Enhancements

- Add support for managed installations of free-threaded Python ([#8100](https://github.com/astral-sh/uv/pull/8100))
- Add note about `uvx` to `uv tool run` short help ([#7695](https://github.com/astral-sh/uv/pull/7695))
- Enable HTTP/2 requests ([#8049](https://github.com/astral-sh/uv/pull/8049))
- Support `uv tree --no-dev` ([#8109](https://github.com/astral-sh/uv/pull/8109))
- Support PEP 723 metadata with `uv run -` ([#8111](https://github.com/astral-sh/uv/pull/8111))
- Support `pip install --exact` ([#8044](https://github.com/astral-sh/uv/pull/8044))
- Support `uv export --no-header` ([#8096](https://github.com/astral-sh/uv/pull/8096))
- Add Python 3.13 images to Docker publish ([#8105](https://github.com/astral-sh/uv/pull/8105))
- Support remote (`https://`) scripts in `uv run` ([#6375](https://github.com/astral-sh/uv/pull/6375))
- Allow comma value-delimited arguments in `uv run --with` ([#7909](https://github.com/astral-sh/uv/pull/7909))

### Configuration

- Support wildcards in `UV_INSECURE_HOST` ([#8052](https://github.com/astral-sh/uv/pull/8052))

### Performance

- Use shared index when fetching metadata in lock satisfaction routine ([#8147](https://github.com/astral-sh/uv/pull/8147))

### Bug fixes

- Add prerelease compatibility check to `uv python` CLI ([#8020](https://github.com/astral-sh/uv/pull/8020))
- Avoid deleting a project environment directory if we cannot tell if a `pyvenv.cfg` file exists ([#8012](https://github.com/astral-sh/uv/pull/8012))
- Avoid excluding valid wheels for exact `requires-python` bounds ([#8140](https://github.com/astral-sh/uv/pull/8140))
- Bump `netrc` crate to latest commit ([#8021](https://github.com/astral-sh/uv/pull/8021))
- Fix `uv python pin 3.13t` failure when parsing version for project requires check ([#8056](https://github.com/astral-sh/uv/pull/8056))
- Fix handling of != intersections in `requires-python` ([#7897](https://github.com/astral-sh/uv/pull/7897))
- Remove the newly created tool environment if sync failed ([#8038](https://github.com/astral-sh/uv/pull/8038))
- Respect dynamic extras in `uv lock` and `uv sync` ([#8091](https://github.com/astral-sh/uv/pull/8091))
- Treat resolver failures as fatal in lockfile validation ([#8083](https://github.com/astral-sh/uv/pull/8083))
- Use `git config --get` for author information for improved backwards compatibility ([#8101](https://github.com/astral-sh/uv/pull/8101))
- Use comma-separated values for `UV_FIND_LINKS` ([#8061](https://github.com/astral-sh/uv/pull/8061))
- Use shared resolver state between add and lock to avoid double Git update ([#8146](https://github.com/astral-sh/uv/pull/8146))
- Make `--relocatable` entrypoints robust to symlinking ([#8079](https://github.com/astral-sh/uv/pull/8079))
- Improve compatibility with VSCode PS1 prompt ([#8006](https://github.com/astral-sh/uv/pull/8006))
- Fix "Stream did not contain valid UTF-8" failures in Windows ([#8120](https://github.com/astral-sh/uv/pull/8120))
- Use `--with-requirements` in `uvx` error hint ([#8112](https://github.com/astral-sh/uv/pull/8112))

### Documentation

- Include `uvx` installation in Docker examples ([#8179](https://github.com/astral-sh/uv/pull/8179))
- Make the instructions for the Windows standalone installer consistent across README and documentation ([#8125](https://github.com/astral-sh/uv/pull/8125))
- Update pip compatibility guide to note transitive URL dependency support ([#8081](https://github.com/astral-sh/uv/pull/8081))
- Document `--reinstall` with `--exclude-newer` to ensure downgrades ([#6721](https://github.com/astral-sh/uv/pull/6721))

## 0.4.20

### Enhancements

- Add managed downloads for CPython 3.13.0 (final) ([#8010](https://github.com/astral-sh/uv/pull/8010))
- Python 3.13 is the default version for `uv python install` ([#8010](https://github.com/astral-sh/uv/pull/8010))
- Hint at wrong endpoint in `uv publish` failures ([#7872](https://github.com/astral-sh/uv/pull/7872))
- List available scripts when a command is not specified for `uv run` ([#7687](https://github.com/astral-sh/uv/pull/7687))
- Fill in `authors` field during `uv init` ([#7756](https://github.com/astral-sh/uv/pull/7756))

### Documentation

- Add snapshot testing to contribution guide ([#7882](https://github.com/astral-sh/uv/pull/7882))
- Fix and improve GitLab integration docs ([#8000](https://github.com/astral-sh/uv/pull/8000))

## 0.4.19

### Enhancements

- Add managed downloads for CPython 3.13.0rc3 and 3.12.7 ([#7880](https://github.com/astral-sh/uv/pull/7880))
- Display the target virtual environment path if non-default ([#7850](https://github.com/astral-sh/uv/pull/7850))
- Preserve case-insensitive sorts in `uv add` ([#7864](https://github.com/astral-sh/uv/pull/7864))
- Respect project upper bounds when filtering wheels on `requires-python` ([#7904](https://github.com/astral-sh/uv/pull/7904))
- Add `--script` to `uv run` to treat an input as PEP 723 regardless of extension ([#7739](https://github.com/astral-sh/uv/pull/7739))
- Improve legibility of build failure errors ([#7854](https://github.com/astral-sh/uv/pull/7854))
- Show interpreter source during Python discovery query errors ([#7928](https://github.com/astral-sh/uv/pull/7928))

### Configuration

- Add `UV_FIND_LINKS` environment variable for `--find-links` ([#7912](https://github.com/astral-sh/uv/pull/7912))
- Ignore empty string values for `UV_PYTHON` environment variable ([#7878](https://github.com/astral-sh/uv/pull/7878))

### Bug fixes

- Allow `py3x-none` tags in newer than Python 3.x ([#7867](https://github.com/astral-sh/uv/pull/7867))
- Allow self-dependencies in the `dev` section ([#7943](https://github.com/astral-sh/uv/pull/7943))
- Always ignore `cp2` wheels in resolution ([#7902](https://github.com/astral-sh/uv/pull/7902))
- Clear the publish progress bar on retry ([#7921](https://github.com/astral-sh/uv/pull/7921))
- Fix parsing of `gnueabi` libc variants in Python version requests ([#7975](https://github.com/astral-sh/uv/pull/7975))
- Simplify supported environments when comparing to lockfile ([#7894](https://github.com/astral-sh/uv/pull/7894))
- Trim commits when reading from Git refs ([#7922](https://github.com/astral-sh/uv/pull/7922))
- Use a higher HTTP read timeout when publishing packages ([#7923](https://github.com/astral-sh/uv/pull/7923))
- Remove the first empty line for `uv tree --package foo` ([#7885](https://github.com/astral-sh/uv/pull/7885))

### Documentation

- Add 3.13 support to the platform reference ([#7971](https://github.com/astral-sh/uv/pull/7971))
- Clarify project environment creation ([#7941](https://github.com/astral-sh/uv/pull/7941))
- Fix code block title in Gitlab integration docs ([#7861](https://github.com/astral-sh/uv/pull/7861))
- Fix project guide section on adding a Git dependency ([#7916](https://github.com/astral-sh/uv/pull/7916))
- Fix uninstallation command for Windows ([#7944](https://github.com/astral-sh/uv/pull/7944))
- Clearly specify the minimum supported Windows Server version ([#7946](https://github.com/astral-sh/uv/pull/7946))

### Rust API

- Remove unused `Sha256Reader` ([#7929](https://github.com/astral-sh/uv/pull/7929))
- Remove unnecessary `Deserialize` derives on settings ([#7856](https://github.com/astral-sh/uv/pull/7856))

## 0.4.18

### Enhancements

- Allow multiple source entries for each package in `tool.uv.sources` ([#7745](https://github.com/astral-sh/uv/pull/7745))
- Add `.gitignore` file to `uv build` output directory ([#7835](https://github.com/astral-sh/uv/pull/7835))
- Disable jemalloc on FreeBSD ([#7780](https://github.com/astral-sh/uv/pull/7780))
- Respect `PAGER` env var when paging in `uv help` command ([#5511](https://github.com/astral-sh/uv/pull/5511))
- Support `uv run -m foo` to run a module ([#7754](https://github.com/astral-sh/uv/pull/7754))
- Use a top-level output directory for `uv build` in workspaces ([#7813](https://github.com/astral-sh/uv/pull/7813))
- Update `uv init --package` command to match project name ([#7670](https://github.com/astral-sh/uv/pull/7670))
- Add a custom suggestion for `uv add dotenv` ([#7799](https://github.com/astral-sh/uv/pull/7799))
- Add detailed errors for `tool.uv.sources` deserialization failures ([#7823](https://github.com/astral-sh/uv/pull/7823))
- Improve error message copy for failed builds ([#7849](https://github.com/astral-sh/uv/pull/7849))
- Use `serde-untagged` to improve some untagged enum error messages ([#7822](https://github.com/astral-sh/uv/pull/7822))
- Use build failure hints for `dotenv` errors, rather than in `uv add` ([#7825](https://github.com/astral-sh/uv/pull/7825))

### Configuration

- Add `UV_NO_SYNC` environment variable ([#7752](https://github.com/astral-sh/uv/pull/7752))

### Bug fixes

- Accept `git+` prefix in `tool.uv.sources` ([#7847](https://github.com/astral-sh/uv/pull/7847))
- Allow spaces in path requirements ([#7767](https://github.com/astral-sh/uv/pull/7767))
- Avoid reusing cached downloaded binaries with `--no-binary` ([#7772](https://github.com/astral-sh/uv/pull/7772))
- Correctly trims values during wheel WHEEL file parsing ([#7770](https://github.com/astral-sh/uv/pull/7770))
- Fix `uv tree --invert` for platform dependencies ([#7808](https://github.com/astral-sh/uv/pull/7808))
- Fix encoding mismatch between python child process and uv ([#7757](https://github.com/astral-sh/uv/pull/7757))
- Reject self-dependencies in `uv add` ([#7766](https://github.com/astral-sh/uv/pull/7766))
- Respect `tool.uv.environments` for legacy virtual workspace roots ([#7824](https://github.com/astral-sh/uv/pull/7824))
- Retain empty extras on workspace members ([#7762](https://github.com/astral-sh/uv/pull/7762))
- Use file stem when parsing cached wheel names ([#7773](https://github.com/astral-sh/uv/pull/7773))

### Rust API

- Make `FlatDistributions` public ([#7833](https://github.com/astral-sh/uv/pull/7833))

### Documentation

- Fix table of contents sizing ([#7751](https://github.com/astral-sh/uv/pull/7751))
- GitLab Integration documentation ([#6857](https://github.com/astral-sh/uv/pull/6857))
- Update documentation to setup-uv@v3 ([#7807](https://github.com/astral-sh/uv/pull/7807))
- Use `uv publish` instead of twine in docs ([#7837](https://github.com/astral-sh/uv/pull/7837))
- Fix typo in `projects.md` ([#7784](https://github.com/astral-sh/uv/pull/7784))

## 0.4.17

### Enhancements

- Add `uv build --all` to build all packages in a workspace ([#7724](https://github.com/astral-sh/uv/pull/7724))
- Add support for `uv init --script` ([#7565](https://github.com/astral-sh/uv/pull/7565))
- Add support for upgrading build environment for installed tools (`uv tool upgrade --python`) ([#7605](https://github.com/astral-sh/uv/pull/7605))
- Initialize a Git repository in `uv init` ([#5476](https://github.com/astral-sh/uv/pull/5476))
- Respect `--quiet` flag in `uv build` ([#7674](https://github.com/astral-sh/uv/pull/7674))
- Add context message before listing available tools in `uvx` ([#7641](https://github.com/astral-sh/uv/pull/7641))

### Bug fixes

- Don't create Python bytecode files during interpreter discovery ([#7707](https://github.com/astral-sh/uv/pull/7707))
- Escape glob patterns in workspace member discovery ([#7709](https://github.com/astral-sh/uv/pull/7709))
- Avoid prefetching source distributions with unbounded lower-bound ranges ([#7683](https://github.com/astral-sh/uv/pull/7683))

### Documentation

- Add `uv build` and `uv publish` to features overview ([#7716](https://github.com/astral-sh/uv/pull/7716))
- Add documentation on cache versioning ([#7693](https://github.com/astral-sh/uv/pull/7693))
- Spell out the names of the Docker images for easier copy-paste ([#7706](https://github.com/astral-sh/uv/pull/7706))
- Document uv-with-Jupyter workflows ([#7625](https://github.com/astral-sh/uv/pull/7625))
- Note that `uv lock --upgrade-package` retains locked versions ([#7694](https://github.com/astral-sh/uv/pull/7694))

## 0.4.16

### Enhancements

- Add `uv publish` ([#7475](https://github.com/astral-sh/uv/pull/7475))
- Add a `--project` argument to run a command from a project directory ([#7603](https://github.com/astral-sh/uv/pull/7603))
- Display Python implementation when creating environments ([#7652](https://github.com/astral-sh/uv/pull/7652))
- Implement trusted publishing for `uv publish` ([#7548](https://github.com/astral-sh/uv/pull/7548))
- Respect lockfile preferences for `--with` requirements ([#7627](https://github.com/astral-sh/uv/pull/7627))
- Unhide the `--directory` option ([#7653](https://github.com/astral-sh/uv/pull/7653))
- Allow requesting free-threaded Python interpreters ([#7431](https://github.com/astral-sh/uv/pull/7431))
- Show a dedicated PubGrub hint for `--unsafe-best-match` ([#7645](https://github.com/astral-sh/uv/pull/7645))
- Add resolver error checking for conflicting distributions ([#7595](https://github.com/astral-sh/uv/pull/7595))

### Bug fixes

- Avoid adding double-newlines for CRLF ([#7640](https://github.com/astral-sh/uv/pull/7640))
- Avoid retaining forks when `requires-python` range changes ([#7624](https://github.com/astral-sh/uv/pull/7624))
- Determine if pre-release Python downloads should be allowed using the version specifiers ([#7638](https://github.com/astral-sh/uv/pull/7638))
- Fix `link-mode=clone` for directories on Linux ([#7620](https://github.com/astral-sh/uv/pull/7620))
- Improve Python executable name discovery when using alternative implementations ([#7649](https://github.com/astral-sh/uv/pull/7649))
- Require opt-in to use alternative Python implementations ([#7650](https://github.com/astral-sh/uv/pull/7650))
- Use the first pre-release discovered when only pre-release Python versions are available ([#7666](https://github.com/astral-sh/uv/pull/7666))

### Documentation

- Document environment variable that disables printing of virtual environment name in prompt ([#7648](https://github.com/astral-sh/uv/pull/7648))
- Remove double whitespaces from the code ([#7623](https://github.com/astral-sh/uv/pull/7623))
- Use anchorlinks rather than permalinks ([#7626](https://github.com/astral-sh/uv/pull/7626))

### Preview features

- Add build backend scaffolding ([#7662](https://github.com/astral-sh/uv/pull/7662))

## 0.4.15

### Bug fixes

- Revert "Treat invalid platform as more compatible than invalid Python (#7556)" ([#7608](https://github.com/astral-sh/uv/pull/7608))

### Documentation

- Add the execution policy to powershell installs for single versions ([#7602](https://github.com/astral-sh/uv/pull/7602))

## 0.4.14

### Breaking

- Move uvx shell completion to `uvx --generate-shell-completion` ([#7511](https://github.com/astral-sh/uv/pull/7511))

### Enhancements

- Adjust messaging for frozen hint on resolution failure during `uv add` ([#7597](https://github.com/astral-sh/uv/pull/7597))
- Provide resolution hints in case of possible local name conflicts ([#7505](https://github.com/astral-sh/uv/pull/7505))
- Improve Docker image release tagging order and display on `ghcr.io` ([#7568](https://github.com/astral-sh/uv/pull/7568))
- Improve deserialization error messages ([#7598](https://github.com/astral-sh/uv/pull/7598))

### Bug fixes

- Allow system environments during project environment validity check ([#7585](https://github.com/astral-sh/uv/pull/7585))
- Avoid validating workspace members when `--no-sources` is provided ([#7599](https://github.com/astral-sh/uv/pull/7599))
- Fix handling of `sys.base_prefix` collision in interpreter identity check during tool installs ([#7596](https://github.com/astral-sh/uv/pull/7596))
- Make `uv cache prune` robust to unreadable rkyv entries ([#7561](https://github.com/astral-sh/uv/pull/7561))
- Revert "Remove duplicate warning for settings discovery errors (#7384)" ([#7594](https://github.com/astral-sh/uv/pull/7594))

### Documentation

- Fix `-` to `_` in packaged applications document ([#7571](https://github.com/astral-sh/uv/pull/7571))

## 0.4.13

### Enhancements

- Add `socks` support ([#7503](https://github.com/astral-sh/uv/pull/7503))
- Avoid warning about bad Python interpreter links for empty project environment directories ([#7527](https://github.com/astral-sh/uv/pull/7527))
- Improve invalid environment warning messages ([#7544](https://github.com/astral-sh/uv/pull/7544))
- Use more verbose spelling of "virtualenv" during creation ([#7523](https://github.com/astral-sh/uv/pull/7523))
- Do not use a user-facing warning for "Waiting to acquire lock..." message ([#7502](https://github.com/astral-sh/uv/pull/7502))

### Performance

- Use a single buffer for hints on resolver errors ([#7497](https://github.com/astral-sh/uv/pull/7497))

### Bug fixes

- Allow Python pre-releases to be used if they are first on the `PATH` ([#7470](https://github.com/astral-sh/uv/pull/7470))
- Avoid deleting the project environment directory if it is not a virtual environment ([#7522](https://github.com/astral-sh/uv/pull/7522))
- Do not error if the `CACHEDIR.TAG` file exists but cannot be written to ([#7550](https://github.com/astral-sh/uv/pull/7550))
- Treat invalid platform as more compatible than invalid Python ([#7556](https://github.com/astral-sh/uv/pull/7556))
- Use portable paths when serializing sources ([#7504](https://github.com/astral-sh/uv/pull/7504))
- Compute resolver hints using the final reduced derivation tree ([#7546](https://github.com/astral-sh/uv/pull/7546))
- Bump the wheel and sdist cache versions ([#7560](https://github.com/astral-sh/uv/pull/7560))
- Heal cache entries with missing source distributions ([#7559](https://github.com/astral-sh/uv/pull/7559))

### Rust libraries

- Bump minimum supported Rust version from 1.80 -> 1.81

### Documentation

- Add `UV_LINK_MODE` to Docker caching example ([#7510](https://github.com/astral-sh/uv/pull/7510))
- Clarify behavior of of overrides in CLI reference ([#7537](https://github.com/astral-sh/uv/pull/7537))

## 0.4.12

### Enhancements

- Allow users to provide pre-defined metadata for resolution ([#7442](https://github.com/astral-sh/uv/pull/7442))
- Invalidate existing tool environments on Python interpreter mismatch ([#7451](https://github.com/astral-sh/uv/pull/7451))

### Bug fixes

- Avoid fatal error when searching for egg-info with missing directory ([#7498](https://github.com/astral-sh/uv/pull/7498))

### Documentation

- Add note on cache growth for self-hosted GitHub runners ([#5757](https://github.com/astral-sh/uv/pull/5757))

## 0.4.11

### Enhancements

- Add `--no-editable` support to `uv sync` and `uv export` ([#7371](https://github.com/astral-sh/uv/pull/7371))
- Add support for `--only-dev` to `uv sync` and `uv export` ([#7367](https://github.com/astral-sh/uv/pull/7367))
- Add support for remaining pip-supported file extensions ([#7387](https://github.com/astral-sh/uv/pull/7387))
- Generate shell completion for `uvx` ([#7388](https://github.com/astral-sh/uv/pull/7388))
- Include `uv export` command in `requirements.txt` output ([#7374](https://github.com/astral-sh/uv/pull/7374))
- Prune unzipped source distributions in `uv cache prune --ci` ([#7446](https://github.com/astral-sh/uv/pull/7446))
- Warn when trying to `uv sync` a package without build configuration ([#7420](https://github.com/astral-sh/uv/pull/7420))
- Support requests for pre-releases in the `--python` option ([#7335](https://github.com/astral-sh/uv/pull/7335))

### Bug fixes

- Avoid erroneous version warning for `.dist-info` directories ([#7444](https://github.com/astral-sh/uv/pull/7444))
- Avoid removing seed packages for `uv venv --seed` environments ([#7410](https://github.com/astral-sh/uv/pull/7410))
- Avoid unnecessary progress bar initializations ([#7412](https://github.com/astral-sh/uv/pull/7412))
- Error when `tool.uv.sources` contains duplicate package names ([#7383](https://github.com/astral-sh/uv/pull/7383))
- Include `--branch` et al when resolving unnamed URLs in `uv add` ([#7447](https://github.com/astral-sh/uv/pull/7447))
- Include `dev-dependencies` in `--no-sources` invocations ([#7408](https://github.com/astral-sh/uv/pull/7408))
- Include the parent interpreter in Python discovery when `--system` is used ([#7440](https://github.com/astral-sh/uv/pull/7440))
- Respect `--no-sources` in PEP 723 scripts ([#7409](https://github.com/astral-sh/uv/pull/7409))
- Respect `pyproject.toml` credentials from user-provided requirements ([#7474](https://github.com/astral-sh/uv/pull/7474))
- Use consistent PyPI cache bucket ([#7443](https://github.com/astral-sh/uv/pull/7443))
- Use unambiguous relative paths in `uv export` ([#7378](https://github.com/astral-sh/uv/pull/7378))

### Documentation

- Add documentation on platform-specific dependencies ([#7411](https://github.com/astral-sh/uv/pull/7411))
- Add documentation for passing installer options on Linux ([#6839](https://github.com/astral-sh/uv/pull/6839))
- Separate project data from configuration settings ([#7053](https://github.com/astral-sh/uv/pull/7053))

### Error messages

- Hint at missing `project.name` ([#6803](https://github.com/astral-sh/uv/pull/6803))
- Surface dedicated `project.name` error for workspaces ([#7399](https://github.com/astral-sh/uv/pull/7399))
- Remove duplicate warning for settings discovery errors ([#7384](https://github.com/astral-sh/uv/pull/7384))

## 0.4.10

### Enhancements

- Allow `uv tool upgrade --all` to continue on individual upgrade failure ([#7333](https://github.com/astral-sh/uv/pull/7333))
- Support globs as cache keys in `tool.uv.cache-keys` ([#7268](https://github.com/astral-sh/uv/pull/7268))
- Add Python package (`__main__.py`) support to `uv run` ([#7281](https://github.com/astral-sh/uv/pull/7281))
- Add zip application support to `uv run` ([#7289](https://github.com/astral-sh/uv/pull/7289))
- Add `--token` option to `self update` command ([#7279](https://github.com/astral-sh/uv/pull/7279))

### Performance

- Use `globwalk` for `cache-keys` matching ([#7337](https://github.com/astral-sh/uv/pull/7337))

### Bug fixes

- Always treat archive-like requirements as local files ([#7364](https://github.com/astral-sh/uv/pull/7364))
- Apply `--no-install` options when constructing resolution ([#7277](https://github.com/astral-sh/uv/pull/7277))
- Avoid clobbering existing `py.typed` files contents in `uv init` ([#7338](https://github.com/astral-sh/uv/pull/7338))
- Avoid enforcing platform compatibility when validating lockfile ([#7305](https://github.com/astral-sh/uv/pull/7305))
- Avoid installing transitive dev dependencies ([#7318](https://github.com/astral-sh/uv/pull/7318))
- Avoid selecting prerelease Python installations without opt-in ([#7300](https://github.com/astral-sh/uv/pull/7300))
- Fix PPC64 page size in binary builds. ([#7298](https://github.com/astral-sh/uv/pull/7298))
- Include pre-release Python versions in `uv python list` ([#7290](https://github.com/astral-sh/uv/pull/7290))
- Make version ID optional for source builds ([#7362](https://github.com/astral-sh/uv/pull/7362))
- Support relative paths in `uv add --script` ([#7301](https://github.com/astral-sh/uv/pull/7301))

### Documentation

- Fix documentation typos for `uv build --build-constraint` flag ([#7330](https://github.com/astral-sh/uv/pull/7330))
- Fix grammatical error in CLI docs ([#7353](https://github.com/astral-sh/uv/pull/7353))

### Error messages

- Add dedicated lock errors for wheel-only distributions ([#7307](https://github.com/astral-sh/uv/pull/7307))
- Avoid treating `.whl` sources as source distributions ([#7303](https://github.com/astral-sh/uv/pull/7303))
- Clarify Python requirement source for script incompatibilities ([#7339](https://github.com/astral-sh/uv/pull/7339))

## 0.4.9

### Enhancements

- Add support for managed Python 3.13 ([#7263](https://github.com/astral-sh/uv/pull/7263))
- Upgrade managed CPython versions to latest patch releases ([#7263](https://github.com/astral-sh/uv/pull/7263))
- Allow setting a target version for `uv self update` ([#7252](https://github.com/astral-sh/uv/pull/7252))
- Create `py.typed` files during `uv init --lib` ([#7232](https://github.com/astral-sh/uv/pull/7232))
- Add a dedicated error for packages that fail due to `distutils` deprecation ([#7239](https://github.com/astral-sh/uv/pull/7239))
- Improve error message when requested Python version is unsupported ([#7269](https://github.com/astral-sh/uv/pull/7269))
- Add `uv run --no-sync` ([#7192]((https://github.com/astral-sh/uv/pull/7192))

### Bug fixes

- Avoid updating `pyproject.toml` offsets on non-add edits ([#7262](https://github.com/astral-sh/uv/pull/7262))
- Invalidate cache when `--config-settings` change ([#7139](https://github.com/astral-sh/uv/pull/7139))
- Remove workspace root for single-member workspace with `uv export` ([#7254](https://github.com/astral-sh/uv/pull/7254))

## 0.4.8

### Enhancements

- Add support for dynamic cache keys ([#7136](https://github.com/astral-sh/uv/pull/7136))
- Allow `.dist-info` names with dashes for post releases ([#7208](https://github.com/astral-sh/uv/pull/7208))
- Use type hints in code from `uv init` ([#7225](https://github.com/astral-sh/uv/pull/7225))
- Treat `.tgz` the same as `.tar.gz` ([#7201](https://github.com/astral-sh/uv/pull/7201))
- Direct users towards `uv venv` to create a virtual environment ([#7188](https://github.com/astral-sh/uv/pull/7188))
- Improve error message for uv init already init-ed ([#7198](https://github.com/astral-sh/uv/pull/7198))

### Performance

- Avoid batch prefetching for un-optimized registries ([#7226](https://github.com/astral-sh/uv/pull/7226))
- Avoid iteration for singleton selections ([#7195](https://github.com/astral-sh/uv/pull/7195))

### Bug fixes

- Avoid extra newlines in debug logging for source builds ([#7174](https://github.com/astral-sh/uv/pull/7174))
- Prune unreachable packages from `--universal` output ([#7209](https://github.com/astral-sh/uv/pull/7209))
- Respect exclusion when collecting workspace members ([#7175](https://github.com/astral-sh/uv/pull/7175))
- Use path file instead of `sitecustomize.py` ([#7161](https://github.com/astral-sh/uv/pull/7161))
- Replace incorrect `--source` and `--binary` flags with correct `--sdist` and `--wheel` flags in `uv build` ([#7156](https://github.com/astral-sh/uv/pull/7156))

### Documentation

- Document support for `UV_INSTALL_DIR` ([#7107](https://github.com/astral-sh/uv/pull/7107))
- List all supported sdist formats ([#7168](https://github.com/astral-sh/uv/pull/7168))

## 0.4.7

### Enhancements

- Add `--no-emit-project` and friends to `uv export` ([#7110](https://github.com/astral-sh/uv/pull/7110))
- Add `--output-file` to `uv export` ([#7109](https://github.com/astral-sh/uv/pull/7109))
- Prune unused source distributions from the cache in `uv cache prune` ([#7112](https://github.com/astral-sh/uv/pull/7112))
- Take intersection of constraint and requirements hashes ([#7108](https://github.com/astral-sh/uv/pull/7108))

### Performance

- Skip metadata fetch for `--no-deps` and `pip sync` ([#7127](https://github.com/astral-sh/uv/pull/7127))

### Bug fixes

- Avoid panicking when encountering an invalid Python version during `uv python list` ([#7131](https://github.com/astral-sh/uv/pull/7131))
- Write trailing newline to `.python-version` files ([#7140](https://github.com/astral-sh/uv/pull/7140))

## 0.4.6

### Enhancements

- Accept `--build-constraint` in `uv build` ([#7085](https://github.com/astral-sh/uv/pull/7085))
- Add `--require-hashes` and `--verify-hashes` to `uv build` ([#7094](https://github.com/astral-sh/uv/pull/7094))
- Add `--show-version-specifiers` to `uv tool list` ([#7050](https://github.com/astral-sh/uv/pull/7050))
- Respect hashes in constraints files ([#7093](https://github.com/astral-sh/uv/pull/7093))
- Upgrade installer scripts ([#7092](https://github.com/astral-sh/uv/pull/7092))
- Allow specifying multiple packages in `uv tool upgrade` and `uninstall` ([#7037](https://github.com/astral-sh/uv/pull/7037))
- Sort by implementation in `uv python list` ([#6918](https://github.com/astral-sh/uv/pull/6918))

### Bug fixes

- Invalidate lockfile when member versions change ([#7102](https://github.com/astral-sh/uv/pull/7102))
- Strip fragments from direct source URLs in lockfile ([#7061](https://github.com/astral-sh/uv/pull/7061))
- Support `--no-build` and `--no-binary` in `uv sync` et al ([#7100](https://github.com/astral-sh/uv/pull/7100))
- Use distribution hash over registry hash ([#7060](https://github.com/astral-sh/uv/pull/7060))
- Fix inverted log message ([#7063](https://github.com/astral-sh/uv/pull/7063))
- Adjust Docker `ENTRYPOINT` and `CMD` for inherited images ([#7054](https://github.com/astral-sh/uv/pull/7054))

### Documentation

- Add winget to installers ([#7088](https://github.com/astral-sh/uv/pull/7088))
- Document how to disable path modifications during install ([#7090](https://github.com/astral-sh/uv/pull/7090))
- Document how to manually update locked package version ([#7083](https://github.com/astral-sh/uv/pull/7083))
- Document official `setup-uv` action ([#7056](https://github.com/astral-sh/uv/pull/7056))
- Update docs on `.python-version` file ([#7051](https://github.com/astral-sh/uv/pull/7051))

## 0.4.5

### Enhancements

- Implement `uv build` ([#6895](https://github.com/astral-sh/uv/pull/6895))
- Add `--package` support to `uv build` ([#6990](https://github.com/astral-sh/uv/pull/6990))
- Prune unreachable packages from lockfile ([#6959](https://github.com/astral-sh/uv/pull/6959))
- Prune unreachable wheels from lockfile ([#6961](https://github.com/astral-sh/uv/pull/6961))
- Show build output by default in `uv build` ([#6912](https://github.com/astral-sh/uv/pull/6912))
- Support `uv build --wheel` from source distributions ([#6898](https://github.com/astral-sh/uv/pull/6898))
- Use the root project name for the project virtual environment prompt ([#7021](https://github.com/astral-sh/uv/pull/7021))

### Bug fixes

- Fix handling of inline optional dependencies in `uv add` ([#7023](https://github.com/astral-sh/uv/pull/7023))
- Reflect exit code in `uv tool run` and `uv run` ([#6994](https://github.com/astral-sh/uv/pull/6994))
- Revert `pyproject.toml` modifications on Ctrl-C ([#7024](https://github.com/astral-sh/uv/pull/7024))
- Rollback `pyproject.toml` changes on all errors ([#7022](https://github.com/astral-sh/uv/pull/7022))
- Use correct ordering semantics for narrowing upper-bounded Python requirements ([#7031](https://github.com/astral-sh/uv/pull/7031))
- Fix segfault in Windows trampolines ([#6955](https://github.com/astral-sh/uv/pull/6955))
- Remove unused `__future__.annotations` import in `_virtualenv.py` ([#6996](https://github.com/astral-sh/uv/pull/6996))

### Documentation

- Add documentation for `uv build` ([#6991](https://github.com/astral-sh/uv/pull/6991))
- Add note to `extra` and `all-extras` in `uv sync` help ([#7013](https://github.com/astral-sh/uv/pull/7013))
- Add project docs for `project.scripts` ([#7010](https://github.com/astral-sh/uv/pull/7010))
- Fix available Docker image tag rendering and shorten list ([#7017](https://github.com/astral-sh/uv/pull/7017))
- Touchup to the project environment config section ([#7038](https://github.com/astral-sh/uv/pull/7038))
- Clarify precedence of `uv.toml` ([#6986](https://github.com/astral-sh/uv/pull/6986))
- Fix available Docker tags for `-slim` variants ([#7041](https://github.com/astral-sh/uv/pull/7041))

## 0.4.4

### Enhancements

- Allow customizing the project environment path with `UV_PROJECT_ENVIRONMENT` ([#6834](https://github.com/astral-sh/uv/pull/6834))
- Warn when `VIRTUAL_ENV` is set but will not be respected in project commands ([#6864](https://github.com/astral-sh/uv/pull/6864))
- Add `--no-hashes` to `uv export` ([#6954](https://github.com/astral-sh/uv/pull/6954))
- Make HTTP headers title case for backward compatibility ([#6887](https://github.com/astral-sh/uv/pull/6887))
- Pin `.python-version` in `uv init` ([#6869](https://github.com/astral-sh/uv/pull/6869))
- Support `file://` URLs for `UV_PYTHON_INSTALL_MIRROR` ([#6950](https://github.com/astral-sh/uv/pull/6950))
- Introduce more docker tags for uv ([#6053](https://github.com/astral-sh/uv/pull/6053))

### Bug fixes

- Avoid canonicalizing the cache directory ([#6949](https://github.com/astral-sh/uv/pull/6949))
- Show all PyPy versions in `uv python list --all-versions` ([#6917](https://github.com/astral-sh/uv/pull/6917))
- Avoid incorrect `requires-python` marker simplifications ([#6268](https://github.com/astral-sh/uv/pull/6268))

### Documentation

- Add documentation for `UV_PROJECT_ENVIRONMENT` ([#6987](https://github.com/astral-sh/uv/pull/6987))
- Add optional dependencies section to the lockfile document ([#6982](https://github.com/astral-sh/uv/pull/6982))
- Document use of the `file://` scheme in Python installation mirrors ([#6984](https://github.com/astral-sh/uv/pull/6984))
- Fix outdated references to the help menu documentation in the first steps page ([#6980](https://github.com/astral-sh/uv/pull/6980))
- Show env option in CLI reference documentation ([#6863](https://github.com/astral-sh/uv/pull/6863))
- Add bind mount example to `docker.md` ([#6921](https://github.com/astral-sh/uv/pull/6921))

## 0.4.3

### Enhancements

- Show build backend output when `--verbose` is provided ([#6903](https://github.com/astral-sh/uv/pull/6903))
- Allow `uv sync --frozen --package` without copying member `pyproject.toml` ([#6943](https://github.com/astral-sh/uv/pull/6943))

### Bug fixes

- Avoid panic with missing temporary directory ([#6929](https://github.com/astral-sh/uv/pull/6929))
- Avoid updating incorrect dependencies for sorted `uv add` ([#6939](https://github.com/astral-sh/uv/pull/6939))
- Use lower-bound semantics for all Python compatibility comparisons ([#6882](https://github.com/astral-sh/uv/pull/6882))

## 0.4.2

### Enhancements

- Adding support for `.pyc` files in `uv run` ([#6886](https://github.com/astral-sh/uv/pull/6886))
- Treat missing `top_level.txt` as non-fatal ([#6881](https://github.com/astral-sh/uv/pull/6881))

### Bug fixes

- Fix `is_disjoint` check for supported environments ([#6902](https://github.com/astral-sh/uv/pull/6902))
- Remove dangling archives in `uv cache clean ${package}` ([#6915](https://github.com/astral-sh/uv/pull/6915))
- Error when discovered Python is incompatible with `--isolated` workspace ([#6885](https://github.com/astral-sh/uv/pull/6885))
- Warn when discovered Python is incompatible with PEP 723 script ([#6884](https://github.com/astral-sh/uv/pull/6884))

## 0.4.1

### Enhancements

- Add `uv export --format requirements-txt` ([#6778](https://github.com/astral-sh/uv/pull/6778))
- Allow `@` references in `uv tool install --from` ([#6842](https://github.com/astral-sh/uv/pull/6842))
- Normalize version specifiers by sorting ([#6333](https://github.com/astral-sh/uv/pull/6333))
- Respect the user's upper-bound in `requires-python` ([#6824](https://github.com/astral-sh/uv/pull/6824))
- Use Windows registry to discover Python on Windows directly ([#6761](https://github.com/astral-sh/uv/pull/6761))
- Hint at `--no-workspace` in `uv init` failures ([#6815](https://github.com/astral-sh/uv/pull/6815))
- Update to last PyPy releases ([#6784](https://github.com/astral-sh/uv/pull/6784))

### Bug fixes

- Avoid deadlocks when multiple uv processes lock resources ([#6790](https://github.com/astral-sh/uv/pull/6790))
- Expand tildes when matching against `PATH` ([#6829](https://github.com/astral-sh/uv/pull/6829))
- Fix `uv init --no-project` alias ([#6837](https://github.com/astral-sh/uv/pull/6837))
- Ignore pre-release segments when discovering via `requires-python` ([#6813](https://github.com/astral-sh/uv/pull/6813))
- Support inline optional tables in `uv add` and `uv remove` ([#6787](https://github.com/astral-sh/uv/pull/6787))
- Update default `hello.py` to pass `ruff format` ([#6811](https://github.com/astral-sh/uv/pull/6811))
- Avoid stripping root for user path display ([#6865](https://github.com/astral-sh/uv/pull/6865))
- Error when user-provided environments are disjoint with Python ([#6841](https://github.com/astral-sh/uv/pull/6841))
- Retain alphabetical sorting for `pyproject.toml` in `uv add` operations ([#6388](https://github.com/astral-sh/uv/pull/6388))))

### Documentation

- Add a link to the multiple index docs in the alternative index guide ([#6826](https://github.com/astral-sh/uv/pull/6826))
- Add docs for inline exclude newer in PEP 723 scripts ([#6831](https://github.com/astral-sh/uv/pull/6831))
- Enumerate available Docker tags ([#6768](https://github.com/astral-sh/uv/pull/6768))
- Omit `[pip]` section from configuration file docs ([#6814](https://github.com/astral-sh/uv/pull/6814))
- Update `project.urls` in `pyproject.toml` ([#6844](https://github.com/astral-sh/uv/pull/6844))
- Add docs for AWS CodeArtifact usage ([#6816](https://github.com/astral-sh/uv/pull/6816))

### Other changes

## 0.4.0

This release adds first-class support for Python projects that are not designed as Python packages (e.g., web applications, data science projects, etc.).

In doing so, it includes some breaking changes around uv's handling of projects. Previously, uv required that all projects could be built into distributable Python packages, and installed them into the virtual environment. Projects created by `uv init` always included a `[build-system]` definition and existing projects that did not define a `[build-system]` would use the legacy setuptools build backend by default.

Most users are not developing libraries that need to be packaged and published to PyPI. Instead, they're building applications using web frameworks, or running collections of Python scripts in the project's root directory. In these cases, requiring a `[build-system]` was confusing and error-prone. In this release, uv changes the default behavior to orient around these common use cases.

In summary, the major changes are:

- uv no longer attempts to package and install projects that do not define a `[build-system]`.
  - While the project itself will not be installed into the virtual environment, its dependencies will still be included.
  - The previous behavior can be recovered by setting `package = true` in the `[tool.uv]` section of your `pyproject.toml`.
- `uv init` no longer creates a `src/` directory or defines a `[build-system]` by default.
  - The previous behavior can be recovered with `uv init --lib` or `uv init --app --package`.
- uv allows and recommends including `[project]` definitions in virtual workspace roots.
  - Previously, the uv required the `[project]` section to be omitted.
- uv allows disabling packaging of projects, even if they define a `[build-system]`, by setting `package = false` in the `[tool.uv]` section of your `pyproject.toml`.

See the latest documentation on [build systems in projects](http://docs.astral.sh/uv/concepts/projects/#build-systems) for more details.

### Enhancements

- Add first-class support for non-packaged projects ([#6585](https://github.com/astral-sh/uv/pull/6585))
- Add `--app` and `--lib` options to `uv init` ([#6689](https://github.com/astral-sh/uv/pull/6689))
- Use `virtual` source label in lockfile for non-packaged dependencies ([#6728](https://github.com/astral-sh/uv/pull/6728))
- Read hash from URL fragment if `--hashes` are omitted ([#6731](https://github.com/astral-sh/uv/pull/6731))
- Support `{package}@{version}` in `uv tool install` ([#6762](https://github.com/astral-sh/uv/pull/6762))
- Publish additional Docker tags without patch version ([#6734](https://github.com/astral-sh/uv/pull/6734))

### Bug fixes

- Accept either strings or structs for hosts ([#6763](https://github.com/astral-sh/uv/pull/6763))
- Avoid including non-excluded members in parent workspaces ([#6735](https://github.com/astral-sh/uv/pull/6735))
- Avoid reading stale `.egg-info` from mutable sources ([#6714](https://github.com/astral-sh/uv/pull/6714))
- Avoid writing invalid PEP 723 scripts on `tool.uv.sources` ([#6706](https://github.com/astral-sh/uv/pull/6706))
- Compare virtual members when invalidating lockfile ([#6754](https://github.com/astral-sh/uv/pull/6754))
- Do not require workspace members to sync with `--frozen` ([#6737](https://github.com/astral-sh/uv/pull/6737))
- Implement deserialization for trusted host ([#6716](https://github.com/astral-sh/uv/pull/6716))
- Avoid showing duplicate paths in `uv python list` ([#6740](https://github.com/astral-sh/uv/pull/6740))
- Raise an error for unclosed script tags in PEP 723 scripts ([#6704](https://github.com/astral-sh/uv/pull/6704))

### Documentation

- Add dependabot and renovate documentation page ([#6236](https://github.com/astral-sh/uv/pull/6236))
- Bind to the host to allow connections in FastAPI Docker example ([#6753](https://github.com/astral-sh/uv/pull/6753))
- Fix some broken links ([#6705](https://github.com/astral-sh/uv/pull/6705))
- Update FastAPI guide for virtual projects and use `uv init` to create the `pyproject.toml` ([#6752](https://github.com/astral-sh/uv/pull/6752))
- Update project documentation for the application / library concepts ([#6718](https://github.com/astral-sh/uv/pull/6718))
- Update workspace documentation to remove legacy virtual projects ([#6720](https://github.com/astral-sh/uv/pull/6720))

## 0.3.5

### Enhancements

- Add support for `--allow-insecure-host` (aliased to `--trusted-host`) ([#6591](https://github.com/astral-sh/uv/pull/6591))
- Read requirements from `requires.txt` when available ([#6655](https://github.com/astral-sh/uv/pull/6655))
- Respect `tool.uv.environments` in `pip compile --universal` ([#6663](https://github.com/astral-sh/uv/pull/6663))
- Use relative paths by default in `uv add` ([#6686](https://github.com/astral-sh/uv/pull/6686))
- Improve messages for empty solves and installs ([#6588](https://github.com/astral-sh/uv/pull/6588))

### Bug fixes

- Avoid reusing state across tool upgrades ([#6660](https://github.com/astral-sh/uv/pull/6660))
- Detect musl and error for musl Python builds ([#6643](https://github.com/astral-sh/uv/pull/6643))
- Ignore `send` errors in installer ([#6667](https://github.com/astral-sh/uv/pull/6667))

### Documentation

- Add development section to Docker guide and reference new example project ([#6666](https://github.com/astral-sh/uv/pull/6666))
- Add docs for `constraint-dependencies` and `override-dependencies` ([#6596](https://github.com/astral-sh/uv/pull/6596))
- Clarify package priority order in pip compatibility guide ([#6619](https://github.com/astral-sh/uv/pull/6619))
- Fix docs for disabling build isolation with `uv sync` ([#6674](https://github.com/astral-sh/uv/pull/6674))
- Improve consistency of directory lookup instructions in Docker ([#6665](https://github.com/astral-sh/uv/pull/6665))
- Improve lockfile concept documentation, add coverage for upgrades ([#6698](https://github.com/astral-sh/uv/pull/6698))
- Shift the order of some of the Docker guide content ([#6664](https://github.com/astral-sh/uv/pull/6664))
- Use `python` to highlight requirements and use more content tabs ([#6549](https://github.com/astral-sh/uv/pull/6549))

## 0.3.4

### CLI

- Show `--editable` on the `uv add` CLI ([#6608](https://github.com/astral-sh/uv/pull/6608))
- Add `--refresh` to `tool run` warning for `--with` dependencies ([#6609](https://github.com/astral-sh/uv/pull/6609))

### Bug fixes

- Allow per dependency build isolation for `setup.py`-based projects ([#6517](https://github.com/astral-sh/uv/pull/6517))
- Avoid un-strict syncing by-default for build isolation ([#6606](https://github.com/astral-sh/uv/pull/6606))
- Respect `--no-build-isolation-package` in `uv sync` ([#6605](https://github.com/astral-sh/uv/pull/6605))
- Respect extras and markers on virtual dev dependencies ([#6620](https://github.com/astral-sh/uv/pull/6620))
- Support PEP 723 scripts in GUI files ([#6611](https://github.com/astral-sh/uv/pull/6611))
- Update lockfile after setting minimum bounds in `uv add` ([#6618](https://github.com/astral-sh/uv/pull/6618))
- Use relative paths for `--find-links` and local registries ([#6566](https://github.com/astral-sh/uv/pull/6566))
- Use separate types to represent raw vs. resolver markers ([#6646](https://github.com/astral-sh/uv/pull/6646))
- Parse wheels `WHEEL` and `METADATA` files as email messages ([#6616](https://github.com/astral-sh/uv/pull/6616))
- Support unquoted hrefs in `--find-links` and other HTML sources ([#6622](https://github.com/astral-sh/uv/pull/6622))
- Don't canonicalize paths to user requirements ([#6560](https://github.com/astral-sh/uv/pull/6560))

### Documentation

- Add FastAPI guide to overview ([#6603](https://github.com/astral-sh/uv/pull/6603))
- Add docs for disabling build isolation with `uv sync` ([#6607](https://github.com/astral-sh/uv/pull/6607))
- Add example of reading script from stdin using echo ([#6567](https://github.com/astral-sh/uv/pull/6567))
- Add tip to use intermediate layers in Docker builds ([#6650](https://github.com/astral-sh/uv/pull/6650))
- Clarify need to include `pyproject.toml` with `--no-install-project` ([#6581](https://github.com/astral-sh/uv/pull/6581))
- Move `WORKDIR` directive in Docker examples ([#6652](https://github.com/astral-sh/uv/pull/6652))
- Remove duplicate `WORKDIR` directive in Docker example ([#6651](https://github.com/astral-sh/uv/pull/6651))

## 0.3.3

### Enhancements

- Add `uv sync --no-install-project` to skip installation of the project ([#6538](https://github.com/astral-sh/uv/pull/6538))
- Add `uv sync --no-install-workspace` to skip installation of all workspace members ([#6539](https://github.com/astral-sh/uv/pull/6539))
- Add `uv sync --no-install-package` to skip installation of specific packages ([#6540](https://github.com/astral-sh/uv/pull/6540))
- Show previous version in self update message ([#6473](https://github.com/astral-sh/uv/pull/6473))

### CLI

- Add `--no-project` alias for `uv python pin --no-workspace` ([#6514](https://github.com/astral-sh/uv/pull/6514))
- Ignore `.python-version` files in `uv venv` with `--no-config` ([#6513](https://github.com/astral-sh/uv/pull/6513))
- Include virtual environment interpreters in `uv python find` ([#6521](https://github.com/astral-sh/uv/pull/6521))
- Respect `-` as stdin channel for `uv run` ([#6481](https://github.com/astral-sh/uv/pull/6481))
- Revert changes to pyproject.toml when sync fails during `uv add` ([#6526](https://github.com/astral-sh/uv/pull/6526))

### Configuration

- Add `UV_COMPILE_BYTECODE` environment variable ([#6530](https://github.com/astral-sh/uv/pull/6530))

### Bug fixes

- Set `VIRTUAL_ENV` for `uv run` invocations ([#6543](https://github.com/astral-sh/uv/pull/6543))
- Ignore errors in workspace discovery with `--no-project` ([#6554](https://github.com/astral-sh/uv/pull/6554))

### Documentation

- Add documentation for `uv python find` ([#6527](https://github.com/astral-sh/uv/pull/6527))
- Add uv tool install example in Docker ([#6547](https://github.com/astral-sh/uv/pull/6547))
- Document why we do lower bounds ([#6516](https://github.com/astral-sh/uv/pull/6516))
- Fix to miss string termination in PowerShell commands for shell autocompletion documentation ([#6491](https://github.com/astral-sh/uv/pull/6491))
- Fix incorrect workspace members keyword ([#6502](https://github.com/astral-sh/uv/pull/6502))
- Use proper environment variables for Windows ([#6433](https://github.com/astral-sh/uv/pull/6433))
- Improve caveat in `uvx` note ([#6546](https://github.com/astral-sh/uv/pull/6546))

## 0.3.2

### Configuration

- Add support for configuring `python-downloads` with `UV_PYTHON_DOWNLOADS` ([#6436](https://github.com/astral-sh/uv/pull/6436))
- Add support for configuring the `python-preference` with `UV_PYTHON_PREFERENCE` ([#6432](https://github.com/astral-sh/uv/pull/6432))
- Deny invalid members in workspace schema ([#6450](https://github.com/astral-sh/uv/pull/6450))

### Performance

- Stop streaming wheels when `METADATA` is discovered (if range requests aren't supported) ([#6470](https://github.com/astral-sh/uv/pull/6470))

### Bug fixes

- Remove URI type from JSON Schema ([#6449](https://github.com/astral-sh/uv/pull/6449))
- Fix retrieval of credentials for URLs from cache ([#6452](https://github.com/astral-sh/uv/pull/6452))
- Restore `cache` suffix on Windows cache path ([#6482](https://github.com/astral-sh/uv/pull/6482))
- Treat `.pyw` files as scripts in `uv run` on Windows ([#6453](https://github.com/astral-sh/uv/pull/6453))
- Treat invalid extras as `false` in marker evaluation ([#6395](https://github.com/astral-sh/uv/pull/6395))
- Avoid overwriting symlinks in `pip compile` output ([#6487](https://github.com/astral-sh/uv/pull/6487))

### Documentation

- Add `uv run` hint to the `uvx` guide ([#6454](https://github.com/astral-sh/uv/pull/6454))
- Add a guide for using uv with FastAPI ([#6401](https://github.com/astral-sh/uv/pull/6401))
- Add tip for using `managed = false` to disable project management ([#6465](https://github.com/astral-sh/uv/pull/6465))
- Clarify the `uv tool run`, `uvx`, and `uv run` relationships ([#6455](https://github.com/astral-sh/uv/pull/6455))
- Fix references to `--python-downloads` (it is `--no-python-downloads`) ([#6439](https://github.com/astral-sh/uv/pull/6439))
- Further clarifications to the tools documentation ([#6474](https://github.com/astral-sh/uv/pull/6474))
- Update docs dockerfile (bullseye -> bookworm) ([#6441](https://github.com/astral-sh/uv/pull/6441))
- Update the installation documentation page ([#6468](https://github.com/astral-sh/uv/pull/6468))
- Update pip compatibility pages to mention configuration files support ([#6410](https://github.com/astral-sh/uv/pull/6410))
- Add `uv run` docs for gui scripts ([#6478](https://github.com/astral-sh/uv/pull/6478))

## 0.3.1

### Enhancements

- Add `--with-editable` support to `uv run` ([#6262](https://github.com/astral-sh/uv/pull/6262))
- Respect `.python-version` files and `pyproject.toml` in `uv python find` ([#6369](https://github.com/astral-sh/uv/pull/6369))
- Allow manylinux compatibility override via `_manylinux` module ([#6039](https://github.com/astral-sh/uv/pull/6039))

### CLI

- Avoid treating `uv add -r` as `--raw-sources` ([#6287](https://github.com/astral-sh/uv/pull/6287))

### Bug fixes

- Always invoke found interpreter when `uv run python` is used ([#6363](https://github.com/astral-sh/uv/pull/6363))
- Avoid adding extra newline for script with non-empty prelude ([#6366](https://github.com/astral-sh/uv/pull/6366))
- Fix metadata cache instability for lockfile ([#6332](https://github.com/astral-sh/uv/pull/6332))
- Handle Ctrl-C properly in `uvx` invocations ([#6346](https://github.com/astral-sh/uv/pull/6346))
- Ignore workspace discovery errors with `--no-workspace` ([#6328](https://github.com/astral-sh/uv/pull/6328))
- Invalidate `uv.lock` when virtual `dev-dependencies` change ([#6291](https://github.com/astral-sh/uv/pull/6291))
- Make cache robust to removed archives ([#6284](https://github.com/astral-sh/uv/pull/6284))
- Preserve Git username for SSH dependencies ([#6335](https://github.com/astral-sh/uv/pull/6335))
- Respect `--no-build-isolation` in `uv add` ([#6368](https://github.com/astral-sh/uv/pull/6368))
- Respect `.python-version` files in `uv run` outside projects ([#6361](https://github.com/astral-sh/uv/pull/6361))
- Use `sys_executable` for `uv run` invocations ([#6354](https://github.com/astral-sh/uv/pull/6354))
- Use atomic write for `pip compile` output ([#6274](https://github.com/astral-sh/uv/pull/6274))
- Use consistent logic for deserializing short revisions ([#6341](https://github.com/astral-sh/uv/pull/6341))

### Documentation

- Remove the preview default value of `python-preference` ([#6301](https://github.com/astral-sh/uv/pull/6301))
- Update env vars doc about `XDG_*` variables on macOS ([#6337](https://github.com/astral-sh/uv/pull/6337))

## 0.3.0

This release introduces the uv [project](https://docs.astral.sh/uv/guides/projects/),
[tool](https://docs.astral.sh/uv/guides/tools/),
[script](https://docs.astral.sh/uv/guides/scripts/), and
[python](https://docs.astral.sh/uv/guides/install-python/) interfaces. If you've been following
uv's development, you've probably seen these new commands behind a preview flag. Now, the
interfaces are stable and ready for production-use.

These features are all documented in [new, comprehensive
documentation](https://docs.astral.sh/uv/).

This release also stabilizes preview functionality in `uv venv`:

- `uv venv --python <version>` will [automatically
download](https://docs.astral.sh/uv/concepts/python-versions/#requesting-a-version) the Python
version if required
- `uv venv` will read the required Python version from the `.python-version` file or
`pyproject.toml`

The `uv pip` interface should not be affected by any breaking changes.

Note the following changelog entries does not include all the new features since they were added
incrementally as preview features. See the
[feature page](https://docs.astral.sh/uv/getting-started/features/) in the documentation for a
comprehensive listing, or read the [blog post](https://astral.sh/blog/uv-unified-python-packaging)
for more context on the new features.

### Breaking changes

- Migrate to XDG and Linux strategy for macOS directories ([#5806](https://github.com/astral-sh/uv/pull/5806))
- Move concurrency settings to top-level ([#4257](https://github.com/astral-sh/uv/pull/4257))
- Apply system Python filtering to executable name requests ([#4309](https://github.com/astral-sh/uv/pull/4309))
- Remove `--legacy-setup-py` command-line argument ([#4255](https://github.com/astral-sh/uv/pull/4255))
- Stabilize preview features ([#6166](https://github.com/astral-sh/uv/pull/6166))

### Enhancements

- Add 32-bit Windows target ([#6252](https://github.com/astral-sh/uv/pull/6252))
- Add support for `python_version in ...` markers ([#6172](https://github.com/astral-sh/uv/pull/6172))
- Allow user to constrain supported lock environments ([#6210](https://github.com/astral-sh/uv/pull/6210))
- Lift requirement that .egg-info filenames must include version ([#6179](https://github.com/astral-sh/uv/pull/6179))
- Change "any of" to "all of" in error messages ([#6222](https://github.com/astral-sh/uv/pull/6222))
- Collapse redundant dependency clauses enumerating available versions ([#6160](https://github.com/astral-sh/uv/pull/6160))
- Collapse unavailable packages in resolver errors ([#6154](https://github.com/astral-sh/uv/pull/6154))
- Fix messages for unavailable packages when range is plural ([#6221](https://github.com/astral-sh/uv/pull/6221))
- Improve resolver error messages when `--offline` is used ([#6156](https://github.com/astral-sh/uv/pull/6156))
- Avoid overwriting dependencies with different markers in `uv add` ([#6010](https://github.com/astral-sh/uv/pull/6010))
- Simplify available package version ranges when the name includes markers or extras ([#6162](https://github.com/astral-sh/uv/pull/6162))
- Simplify version ranges reported for unavailable packages ([#6155](https://github.com/astral-sh/uv/pull/6155))
- Rename `environment-markers` to `resolution-markers` ([#6240](https://github.com/astral-sh/uv/pull/6240))
- Support `uv add -r requirements.txt` ([#6005](https://github.com/astral-sh/uv/pull/6005))

### CLI

- Hide global options in `uv generate-shell-completion` ([#6170](https://github.com/astral-sh/uv/pull/6170))
- Show generate-shell-completion command in `uv help` ([#6180](https://github.com/astral-sh/uv/pull/6180))
- Special-case reinstalls in environment update summaries ([#6243](https://github.com/astral-sh/uv/pull/6243))
- Add output when `uv add` and `uv remove` update scripts ([#6231](https://github.com/astral-sh/uv/pull/6231))
- Add support for `package@latest` in `tool run` ([#6138](https://github.com/astral-sh/uv/pull/6138))
- Show `python find` output with `-q` ([#6256](https://github.com/astral-sh/uv/pull/6256))
- Warn when `--upgrade` is passed to `tool run` ([#6140](https://github.com/astral-sh/uv/pull/6140))

### Configuration

- Allow customizing the tool install directory with `UV_TOOL_BIN_DIR` ([#6207](https://github.com/astral-sh/uv/pull/6207))

### Performance

- Use `FxHash` in `uv-auth` ([#6149](https://github.com/astral-sh/uv/pull/6149))

### Bug fixes

- Avoid panicking when the resolver thread encounters a closed channel ([#6182](https://github.com/astral-sh/uv/pull/6182))
- Respect release-only semantics of `python_full_version` when constructing markers ([#6171](https://github.com/astral-sh/uv/pull/6171))
- Tolerate missing `[project]` table in `uv venv` ([#6178](https://github.com/astral-sh/uv/pull/6178))
- Avoid using workspace `lock_path` as relative root ([#6157](https://github.com/astral-sh/uv/pull/6157))

### Documentation

- Preview changes are now included in the standard changelog ([#6259](https://github.com/astral-sh/uv/pull/6259))
- Document dynamic metadata behavior for cache ([#5993](https://github.com/astral-sh/uv/pull/5993))
- Document the effect of ordering on package priority ([#6211](https://github.com/astral-sh/uv/pull/6211))
- Make some edits to the workspace concept documentation ([#6223](https://github.com/astral-sh/uv/pull/6223))
- Update environment variables doc ([#5994](https://github.com/astral-sh/uv/pull/5994))
- Disable collapsible navigation in the documentation ([#5674](https://github.com/astral-sh/uv/pull/5674))
- Document `uv add` and `uv remove` behavior with markers ([#6163](https://github.com/astral-sh/uv/pull/6163))
- Document the Python installation directory ([#6227](https://github.com/astral-sh/uv/pull/6227))
- Document the `uv.pip` section semantics ([#6225](https://github.com/astral-sh/uv/pull/6225))
- Document the cache directory ([#6229](https://github.com/astral-sh/uv/pull/6229))
- Document the tools directory ([#6228](https://github.com/astral-sh/uv/pull/6228))
- Document yanked packages caveat during sync ([#6219](https://github.com/astral-sh/uv/pull/6219))
- Link to persistent configuration options in Python versions document ([#6226](https://github.com/astral-sh/uv/pull/6226))
- Link to the projects concept from the dependencies concept ([#6224](https://github.com/astral-sh/uv/pull/6224))
- Improvements to the Docker installation guide ([#6216](https://github.com/astral-sh/uv/pull/6216))
- Increase the size of navigation entries ([#6233](https://github.com/astral-sh/uv/pull/6233))
- Install `ca-certificates` in docker and use pipefail ([#6208](https://github.com/astral-sh/uv/pull/6208))
- Add script support to feature highlights in index ([#6251](https://github.com/astral-sh/uv/pull/6251))
- Show `uv generate-shell-completion` in CLI documentation reference ([#6146](https://github.com/astral-sh/uv/pull/6146))
- Update Docker guide for projects ([#6217](https://github.com/astral-sh/uv/pull/6217))
- Use `uv add --script` in guide ([#6215](https://github.com/astral-sh/uv/pull/6215))
- Show pinned version example on in GitHub Actions integration guide ([#6234](https://github.com/astral-sh/uv/pull/6234))

## 0.2.37

### Performance

- Avoid cloning requirement for unchanged markers ([#6116](https://github.com/astral-sh/uv/pull/6116))

### Bug fixes

- Fix loading of cached metadata for Git distributions with
subdirectories ([#6094](https://github.com/astral-sh/uv/pull/6094))

### Error messages

- Add env var to `--link-mode=copy` warning ([#6103](https://github.com/astral-sh/uv/pull/6103))
- Avoid displaying "failed to download" on build failures for local source
distributions ([#6075](https://github.com/astral-sh/uv/pull/6075))
- Improve display of available package ranges ([#6118](https://github.com/astral-sh/uv/pull/6118))
- Use "your requirements" consistently in resolver error messages ([#6113](https://github.com/astral-sh/uv/pull/6113))

### Preview features

- Add `python-version-file` to GitHub integration documentation ([#6086](https://github.com/astral-sh/uv/pull/6086))
- Always narrow markers by Python version ([#6076](https://github.com/astral-sh/uv/pull/6076))
- Avoid warning for redundant `--no-project` ([#6111](https://github.com/astral-sh/uv/pull/6111))
- Change the definition of `--locked` to require satisfaction check ([#6102](https://github.com/astral-sh/uv/pull/6102))
- Improve debug log for interpreter requests during project
commands ([#6120](https://github.com/astral-sh/uv/pull/6120))
- Improve display of resolution errors for workspace member conflicts with optional
dependencies ([#6123](https://github.com/astral-sh/uv/pull/6123))
- Improve resolver error messages for single-project workspaces ([#6095](https://github.com/astral-sh/uv/pull/6095))
- Improve resolver error messages referencing workspace members ([#6092](https://github.com/astral-sh/uv/pull/6092))
- Invalidate `uv.lock` if registry sources are removed ([#6026](https://github.com/astral-sh/uv/pull/6026))
- Propagate fork markers to extras ([#6065](https://github.com/astral-sh/uv/pull/6065))
- Redact Git credentials from `pyproject.toml` ([#6074](https://github.com/astral-sh/uv/pull/6074))
- Redact Git credentials in lockfile ([#6070](https://github.com/astral-sh/uv/pull/6070))
- Remove 'tool' reference on `uv run` CLI ([#6110](https://github.com/astral-sh/uv/pull/6110))
- Remove `same-graph` merging in resolver ([#6077](https://github.com/astral-sh/uv/pull/6077))
- Strip SHA when constructing package source ([#6097](https://github.com/astral-sh/uv/pull/6097))
- Treat Git sources as immutable in lockfile ([#6109](https://github.com/astral-sh/uv/pull/6109))
- Use the proper singular form for workspace member dependencies in resolver
errors ([#6128](https://github.com/astral-sh/uv/pull/6128))
- Use sets rather than vectors for lockfile requirements ([#6107](https://github.com/astral-sh/uv/pull/6107))
- Normalize `python_version` markers to `python_full_version` ([#6126](https://github.com/astral-sh/uv/pull/6126))
- Update Pythons to include Python 3.12.5 ([#6087](https://github.com/astral-sh/uv/pull/6087))

## 0.2.36

### Bug fixes

- Use consistent canonicalization for URLs ([#5980](https://github.com/astral-sh/uv/pull/5980))
- Improve warning message when parsing `pyproject.toml` fails ([#6009](https://github.com/astral-sh/uv/pull/6009))
- Improve handling of overlapping markers in universal resolver ([#5887](https://github.com/astral-sh/uv/pull/5887))

### Preview features

- Add resolver error context to `run` and `tool run` ([#5991](https://github.com/astral-sh/uv/pull/5991))
- Avoid replacing executables on no-op upgrades ([#5998](https://github.com/astral-sh/uv/pull/5998))
- Colocate Python install cache with destination directory ([#6043](https://github.com/astral-sh/uv/pull/6043))
- Filter mixed sources from `--find-links` entries in lockfile ([#6025](https://github.com/astral-sh/uv/pull/6025))
- Fix some outdated documentation discussing Python environments ([#6058](https://github.com/astral-sh/uv/pull/6058))
- Fix projects guide typo ([#6033](https://github.com/astral-sh/uv/pull/6033))
- Fix tools guide typo ([#6027](https://github.com/astral-sh/uv/pull/6027))
- Hide python options in `uv tool list` help ([#6003](https://github.com/astral-sh/uv/pull/6003))
- Improve top-level help for `uv tool` commands ([#5983](https://github.com/astral-sh/uv/pull/5983))
- Move help documentation into dedicated page ([#6057](https://github.com/astral-sh/uv/pull/6057))
- Remove `editable: false` support ([#5987](https://github.com/astral-sh/uv/pull/5987))
- Remove uses of `Option<MarkerTree>` in `ResolutionGraph` ([#6035](https://github.com/astral-sh/uv/pull/6035))
- Resolve relative `tool.uv.sources` relative to containing project ([#6045](https://github.com/astral-sh/uv/pull/6045))
- Support PEP 723 scripts in `uv add` and `uv remove` ([#5995](https://github.com/astral-sh/uv/pull/5995))
- Support `tool.uv` in PEP 723 scripts ([#5990](https://github.com/astral-sh/uv/pull/5990))
- Treat local indexes as registry sources in lockfile ([#6016](https://github.com/astral-sh/uv/pull/6016))
- Use simplified paths in lockfile ([#6049](https://github.com/astral-sh/uv/pull/6049))
- Use upgrade-specific output for tool upgrade ([#5997](https://github.com/astral-sh/uv/pull/5997))

## 0.2.35

### CLI

- Deprecate `--system` and `--no-system` in `uv venv` ([#5925](https://github.com/astral-sh/uv/pull/5925))
- Make `--upgrade` imply `--refresh` ([#5943](https://github.com/astral-sh/uv/pull/5943))
- Warn when there are missing bounds on transitive dependencies
with `--resolution-strategy lowest` ([#5953](https://github.com/astral-sh/uv/pull/5953))

### Configuration

- Add support for `no-build-isolation-package` ([#5894](https://github.com/astral-sh/uv/pull/5894))

### Performance

- Enable LTO optimizations in release builds to reduce binary size ([#5904](https://github.com/astral-sh/uv/pull/5904))
- Prefetch metadata in `--no-deps` mode ([#5918](https://github.com/astral-sh/uv/pull/5918))

### Bug fixes

- Display portable paths in POSIX virtual environment activation
commands ([#5956](https://github.com/astral-sh/uv/pull/5956))
- Respect subdirectories when locating Git workspaces ([#5944](https://github.com/astral-sh/uv/pull/5944))

### Documentation

- Improve the `uv venv` CLI documentation ([#5963](https://github.com/astral-sh/uv/pull/5963))

### Preview features

- Add CLI flags to reference documentation ([#5926](https://github.com/astral-sh/uv/pull/5926))
- Add `update` alias for `uv tool upgrade` ([#5948](https://github.com/astral-sh/uv/pull/5948))
- Add caveat about pip interface name ([#5940](https://github.com/astral-sh/uv/pull/5940))
- Add hint for long help to `uvx` ([#5971](https://github.com/astral-sh/uv/pull/5971))
- Avoid requires-python warning in virtual-only workspace ([#5895](https://github.com/astral-sh/uv/pull/5895))
- Discard forks when using `--upgrade` ([#5905](https://github.com/astral-sh/uv/pull/5905))
- Document the `tool upgrade` command ([#5947](https://github.com/astral-sh/uv/pull/5947))
- Document virtual environment discovery ([#5965](https://github.com/astral-sh/uv/pull/5965))
- Enable mirror for `python-build-standalone` downloads ([#5719](https://github.com/astral-sh/uv/pull/5719))
- Fix reuse of Git commits in lockfile ([#5908](https://github.com/astral-sh/uv/pull/5908))
- Ignore local configuration in tool commands ([#5923](https://github.com/astral-sh/uv/pull/5923))
- Improve the CLI documentation for `uv add` ([#5914](https://github.com/astral-sh/uv/pull/5914))
- Improve the CLI documentation for `uv remove` ([#5916](https://github.com/astral-sh/uv/pull/5916))
- Improve the `uv lock` CLI documentation ([#5932](https://github.com/astral-sh/uv/pull/5932))
- Improve the `uv python` CLI documentation ([#5961](https://github.com/astral-sh/uv/pull/5961))
- Improve the `uv sync` CLI documentation ([#5930](https://github.com/astral-sh/uv/pull/5930))
- Improve the `uv tree` CLI documentation ([#5917](https://github.com/astral-sh/uv/pull/5917))
- Fix link to tools concept page ([#5906](https://github.com/astral-sh/uv/pull/5906))
- Add `uv tool upgrade` command ([#5197](https://github.com/astral-sh/uv/pull/5197))
- Implement marker trees using algebraic decision diagrams ([#5898](https://github.com/astral-sh/uv/pull/5898))
- Make repeated `uv add` operations simpler ([#5922](https://github.com/astral-sh/uv/pull/5922))
- Move some documents to relevant sections ([#5968](https://github.com/astral-sh/uv/pull/5968))
- Rename `distribution` to `packages` in lockfile ([#5861](https://github.com/astral-sh/uv/pull/5861))
- Respect `--upgrade-package` in tool install ([#5941](https://github.com/astral-sh/uv/pull/5941))
- Respect `--upgrade-package` when resolving from lockfile ([#5907](https://github.com/astral-sh/uv/pull/5907))
- Retain and respect settings in tool upgrades ([#5937](https://github.com/astral-sh/uv/pull/5937))
- Search beyond workspace root when discovering configuration ([#5931](https://github.com/astral-sh/uv/pull/5931))
- Show build and install summaries in `uv run` and `uv tool run` ([#5899](https://github.com/astral-sh/uv/pull/5899))
- Support relative path wheels ([#5969](https://github.com/astral-sh/uv/pull/5969))
- Update the interface for declaring Python download preferences ([#5936](https://github.com/astral-sh/uv/pull/5936))
- Use cached environments for `--with` layers ([#5897](https://github.com/astral-sh/uv/pull/5897))
- Warn when project-specific settings are passed to non-project `uv run`
commands ([#5977](https://github.com/astral-sh/uv/pull/5977))

## 0.2.34

### Enhancements

- Always strip in release mode ([#5745](https://github.com/astral-sh/uv/pull/5745))
- Assume `git+` prefix when URLs end in `.git` ([#5868](https://github.com/astral-sh/uv/pull/5868))
- Support build constraints ([#5639](https://github.com/astral-sh/uv/pull/5639))

### CLI

- Create help sections for build, install, resolve, and index ([#5693](https://github.com/astral-sh/uv/pull/5693))
- Improve CLI documentation for global options ([#5834](https://github.com/astral-sh/uv/pull/5834))
- Improve `--python` CLI documentation ([#5869](https://github.com/astral-sh/uv/pull/5869))
- Improve display order of top-level commands ([#5830](https://github.com/astral-sh/uv/pull/5830))

### Bug fixes

- Allow downloading wheels for metadata with `--no-binary` ([#5707](https://github.com/astral-sh/uv/pull/5707))
- Reject `pyproject.toml` in `--config-file` ([#5842](https://github.com/astral-sh/uv/pull/5842))
- Remove double-proxy nodes in error reporting ([#5738](https://github.com/astral-sh/uv/pull/5738))
- Respect pre-release preferences from input files ([#5736](https://github.com/astral-sh/uv/pull/5736))
- Support overlapping local and non-local requirements in forks ([#5812](https://github.com/astral-sh/uv/pull/5812))

### Preview features

- Add "next steps" to some early documentation pages ([#5825](https://github.com/astral-sh/uv/pull/5825))
- Add `--no-build-isolation` to uv lock et al ([#5829](https://github.com/astral-sh/uv/pull/5829))
- Add `--no-sources` to avoid reading from `tool.uv.sources` ([#5801](https://github.com/astral-sh/uv/pull/5801))
- Add `uv add --no-sync` and `uv remove --no-sync` ([#5881](https://github.com/astral-sh/uv/pull/5881))
- Add a guide for publishing packages ([#5794](https://github.com/astral-sh/uv/pull/5794))
- Address some feedback in the tools documentation ([#5827](https://github.com/astral-sh/uv/pull/5827))
- Avoid lingering dev and optional dependencies in `uv tree` ([#5766](https://github.com/astral-sh/uv/pull/5766))
- Avoid mismatch in `--locked` with Git dependencies ([#5865](https://github.com/astral-sh/uv/pull/5865))
- Avoid panic when re-locking with precise commit ([#5863](https://github.com/astral-sh/uv/pull/5863))
- Avoid using already-installed tools on `--upgrade`
or `--reinstall` ([#5799](https://github.com/astral-sh/uv/pull/5799))
- Better workspace documentation ([#5728](https://github.com/astral-sh/uv/pull/5728))
- Collapse policies section into reference ([#5696](https://github.com/astral-sh/uv/pull/5696))
- Don't show deprecated warning in `uvx --isolated` ([#5798](https://github.com/astral-sh/uv/pull/5798))
- Ensure `python`-to-`pythonX.Y` symlink exists in downloaded
Pythons ([#5849](https://github.com/astral-sh/uv/pull/5849))
- Fix CLI reference URLs to subcommands ([#5722](https://github.com/astral-sh/uv/pull/5722))
- Fix some console blocks in the environment doc ([#5826](https://github.com/astral-sh/uv/pull/5826))
- Group resolver options in lockfile ([#5853](https://github.com/astral-sh/uv/pull/5853))
- Improve CLI documentation for `uv tree` ([#5870](https://github.com/astral-sh/uv/pull/5870))
- Improve documentation for `uv init` CLI ([#5862](https://github.com/astral-sh/uv/pull/5862))
- Improvements to the documentation ([#5718](https://github.com/astral-sh/uv/pull/5718))
- Link to the GitHub integration guide from the cache concept ([#5828](https://github.com/astral-sh/uv/pull/5828))
- Make some minor tweaks to the docs ([#5786](https://github.com/astral-sh/uv/pull/5786))
- Omit local segments when adding uv add bounds ([#5753](https://github.com/astral-sh/uv/pull/5753))
- Remove top-level bar from Python installs ([#5788](https://github.com/astral-sh/uv/pull/5788))
- Replace `uv help python` references in CLI documentation with
links ([#5871](https://github.com/astral-sh/uv/pull/5871))
- Respect `.python-version` in `--isolated` runs ([#5741](https://github.com/astral-sh/uv/pull/5741))
- Respect malformed `.dist-info` directories in tool installs ([#5756](https://github.com/astral-sh/uv/pull/5756))
- Reuse existing virtualenvs with `--no-project` ([#5846](https://github.com/astral-sh/uv/pull/5846))
- Rewrite resolver docs ([#5723](https://github.com/astral-sh/uv/pull/5723))
- Show default and possible options in CLI reference documentation ([#5720](https://github.com/astral-sh/uv/pull/5720))
- Skip files when detecting workspace members ([#5735](https://github.com/astral-sh/uv/pull/5735))
- Support empty dependencies in PEP 723 scripts ([#5864](https://github.com/astral-sh/uv/pull/5864))
- Support uv add `--dev` in virtual workspaces ([#5821](https://github.com/astral-sh/uv/pull/5821))
- Update documentation index ([#5824](https://github.com/astral-sh/uv/pull/5824))
- Update resolver reference documentation ([#5823](https://github.com/astral-sh/uv/pull/5823))
- Update the override section with some content from the README ([#5820](https://github.com/astral-sh/uv/pull/5820))
- Update the resolution concept documentation ([#5813](https://github.com/astral-sh/uv/pull/5813))
- Use cache for Python install temporary directories ([#5787](https://github.com/astral-sh/uv/pull/5787))
- Use lockfile directly in `uv tree` ([#5761](https://github.com/astral-sh/uv/pull/5761))
- Use uv installer during build ([#5854](https://github.com/astral-sh/uv/pull/5854))
- Filter `uv tree` to current platform by default ([#5763](https://github.com/astral-sh/uv/pull/5763))
- Redact registry credentials in lockfile ([#5803](https://github.com/astral-sh/uv/pull/5803))
- Show extras and dev dependencies in `uv tree` ([#5768](https://github.com/astral-sh/uv/pull/5768))
- Support `--python-platform` in `uv tree` ([#5764](https://github.com/astral-sh/uv/pull/5764))
- Add help heading for `--no-sources` ([#5833](https://github.com/astral-sh/uv/pull/5833))
- Avoid reusing incompatible distributions across lock and sync ([#5845](https://github.com/astral-sh/uv/pull/5845))
- Fix broken anchor links in docs about dependencies ([#5769](https://github.com/astral-sh/uv/pull/5769))
- Fix the default value of python-preference in
docs/reference/settings.md ([#5755](https://github.com/astral-sh/uv/pull/5755))
- Improve CLI documentation for `uv run` ([#5841](https://github.com/astral-sh/uv/pull/5841))
- Remove some trailing backticks from the docs ([#5781](https://github.com/astral-sh/uv/pull/5781))
- Use `uvx` in docs serve contributing command ([#5795](https://github.com/astral-sh/uv/pull/5795))

## 0.2.33

### Enhancements

- Add support for `ksh` to relocatable virtual environments ([#5640](https://github.com/astral-sh/uv/pull/5640))

### CLI

- Add help sections for global options ([#5665](https://github.com/astral-sh/uv/pull/5665))
- Move `--python` and `--python-version` into the "Python options"
help ([#5691](https://github.com/astral-sh/uv/pull/5691))
- Show help specific options (i.e. `--no-pager`) in `uv help` ([#5516](https://github.com/astral-sh/uv/pull/5516))
- Update top-level command descriptions ([#5706](https://github.com/astral-sh/uv/pull/5706))

### Bug fixes

- Remove lingering executables after failed installs ([#5666](https://github.com/astral-sh/uv/pull/5666))
- Switch from heuristic freshness lifetime to hard-coded value ([#5654](https://github.com/astral-sh/uv/pull/5654))

### Documentation

- Don't use equals signs for CLI options with values ([#5704](https://github.com/astral-sh/uv/pull/5704))

### Preview features

- Add `--package` to `uv sync` ([#5656](https://github.com/astral-sh/uv/pull/5656))
- Add documentation for caching the uv cache in GHA ([#5663](https://github.com/astral-sh/uv/pull/5663))
- Avoid persisting `uv add` calls that result in resolver errors ([#5664](https://github.com/astral-sh/uv/pull/5664))
- Bold active nav links for accessibility ([#5673](https://github.com/astral-sh/uv/pull/5673))
- Check idempotence in packse lock scenarios ([#5485](https://github.com/astral-sh/uv/pull/5485))
- Detect python version from python project by default in `uv venv` ([#5592](https://github.com/astral-sh/uv/pull/5592))
- Drop badges from docs landing ([#5617](https://github.com/astral-sh/uv/pull/5617))
- Fix non-registry serialization for receipts ([#5668](https://github.com/astral-sh/uv/pull/5668))
- Generate CLI reference for documentation ([#5685](https://github.com/astral-sh/uv/pull/5685))
- Improve copy of console command examples ([#5397](https://github.com/astral-sh/uv/pull/5397))
- Improve the project guide ([#5626](https://github.com/astral-sh/uv/pull/5626))
- Improve the Python version concepts documentation ([#5638](https://github.com/astral-sh/uv/pull/5638))
- Improve the dependency concept documentation ([#5658](https://github.com/astral-sh/uv/pull/5658))
- Include newly-added optional dependencies in lockfile ([#5686](https://github.com/astral-sh/uv/pull/5686))
- Initialize the cache in `uv init` ([#5669](https://github.com/astral-sh/uv/pull/5669))
- Limit sync after `uv add` ([#5705](https://github.com/astral-sh/uv/pull/5705))
- Move pip-compatibility doc into pip interface section ([#5670](https://github.com/astral-sh/uv/pull/5670))
- Move settings reference to reference section ([#5689](https://github.com/astral-sh/uv/pull/5689))
- Omit the nav bar title when it has no use ([#5316](https://github.com/astral-sh/uv/pull/5316))
- Omit transitive development dependencies from workspace lockfile ([#5646](https://github.com/astral-sh/uv/pull/5646))
- Prioritize forks based on Python narrowing ([#5642](https://github.com/astral-sh/uv/pull/5642))
- Prioritize forks based on upper bounds ([#5643](https://github.com/astral-sh/uv/pull/5643))
- Prompt an early jump to the feature overview during first steps ([#5655](https://github.com/astral-sh/uv/pull/5655))
- Remove breadcrumbs for navigation ([#5676](https://github.com/astral-sh/uv/pull/5676))
- Replace `--python-preference installed` with `managed` ([#5637](https://github.com/astral-sh/uv/pull/5637))
- Set lower bounds in `uv add` ([#5688](https://github.com/astral-sh/uv/pull/5688))
- Simplify GHA `UV_SYSTEM_PYTHON` examples ([#5659](https://github.com/astral-sh/uv/pull/5659))
- Support legacy tool receipts with PEP 508 requirements ([#5679](https://github.com/astral-sh/uv/pull/5679))
- Unhide the experimental top-level commands ([#5700](https://github.com/astral-sh/uv/pull/5700))
- Use "uv" for title of index instead of "Introduction" ([#5677](https://github.com/astral-sh/uv/pull/5677))
- Use fork markers and fork preferences in resolution with lockfile ([#5481](https://github.com/astral-sh/uv/pull/5481))
- Use full requirement when serializing receipt ([#5494](https://github.com/astral-sh/uv/pull/5494))
- Use intersection rather than union for `requires-python` ([#5644](https://github.com/astral-sh/uv/pull/5644))
- `uvx` warn when no executables are available ([#5675](https://github.com/astral-sh/uv/pull/5675))

## 0.2.32

### Enhancements

- Deprecate the `--isolated` flag in favor of `--no-config` ([#5466](https://github.com/astral-sh/uv/pull/5466))
- Re-enable `requires-python` narrowing in forks ([#5583](https://github.com/astral-sh/uv/pull/5583))

### Performance

- Skip copying to empty entries in seekable zip ([#5571](https://github.com/astral-sh/uv/pull/5571))
- Use a consistent buffer size for downloads ([#5569](https://github.com/astral-sh/uv/pull/5569))
- Use a consistent buffer size when writing out zip files ([#5570](https://github.com/astral-sh/uv/pull/5570))

### Bug fixes

- Avoid setting executable permissions on files we might not own ([#5582](https://github.com/astral-sh/uv/pull/5582))
- Statically link liblzma ([#5577](https://github.com/astral-sh/uv/pull/5577))

### Preview features

- Implement `uv run --directory` ([#5566](https://github.com/astral-sh/uv/pull/5566))
- Add `--isolated` support to `uv run` ([#5471](https://github.com/astral-sh/uv/pull/5471))
- Add `--no-workspace` and `--no-project` in lieu of `--isolated` ([#5465](https://github.com/astral-sh/uv/pull/5465))
- Add documentation for cache clearing ([#5517](https://github.com/astral-sh/uv/pull/5517))
- Add forks to lockfile, don't read them yet ([#5480](https://github.com/astral-sh/uv/pull/5480))
- Add links to documentation footer ([#5616](https://github.com/astral-sh/uv/pull/5616))
- Error when multiple git references are provided in `uv add` ([#5502](https://github.com/astral-sh/uv/pull/5502))
- Improvements to the project concept docs ([#5634](https://github.com/astral-sh/uv/pull/5634))
- List installed tools when no command is provided to `uv tool run` ([#5553](https://github.com/astral-sh/uv/pull/5553))
- Make `--directory` a global argument ([#5579](https://github.com/astral-sh/uv/pull/5579))
- Reframe use of `--isolated` in `tool run` ([#5470](https://github.com/astral-sh/uv/pull/5470))
- Remove `--isolated` usages from the `uv python` API ([#5468](https://github.com/astral-sh/uv/pull/5468))
- Rename more use of "lock file" to "lockfile" ([#5629](https://github.com/astral-sh/uv/pull/5629))
- Suppress resolver output by default in `uv run` and `uv tool run` ([#5580](https://github.com/astral-sh/uv/pull/5580))
- Wrap documentation at 100 characters ([#5635](https://github.com/astral-sh/uv/pull/5635))

## 0.2.31

### Enhancements

- Add `--relocatable` flag to `uv venv` ([#5515](https://github.com/astral-sh/uv/pull/5515))
- Support `xz`-compressed packages ([#5513](https://github.com/astral-sh/uv/pull/5513))
- Warn, but don't error, when encountering tilde `.dist-info`
directories ([#5520](https://github.com/astral-sh/uv/pull/5520))

### Bug fixes

- Make `pip list --editable` conflict with `--exclude-editable` ([#5506](https://github.com/astral-sh/uv/pull/5506))
- Add some missing reinstall-refresh calls ([#5497](https://github.com/astral-sh/uv/pull/5497))
- Avoid warning users for missing self-extra lower bounds ([#5518](https://github.com/astral-sh/uv/pull/5518))
- Generate hashes for `--find-links` entries ([#5544](https://github.com/astral-sh/uv/pull/5544))
- Retain editable designation for cached wheel installs ([#5545](https://github.com/astral-sh/uv/pull/5545))
- Use 666 rather than 644 for default permissions ([#5498](https://github.com/astral-sh/uv/pull/5498))
- Retry on incomplete body ([#5555](https://github.com/astral-sh/uv/pull/5555))
- Ban `--no-cache` with `--link-mode=symlink` ([#5519](https://github.com/astral-sh/uv/pull/5519))

### Preview features

- Allow `uv pip install` for unmanaged projects ([#5504](https://github.com/astral-sh/uv/pull/5504))
- Compare simplified paths in Windows exclusion tests ([#5525](https://github.com/astral-sh/uv/pull/5525))
- Respect reinstalls in cached environments ([#5499](https://github.com/astral-sh/uv/pull/5499))
- Use `hatchling` rather than implicit `setuptools` default ([#5527](https://github.com/astral-sh/uv/pull/5527))
- Use relocatable installs to support concurrency-safe cached
environments ([#5509](https://github.com/astral-sh/uv/pull/5509))
- Support `--editable` installs for `uv tool` ([#5454](https://github.com/astral-sh/uv/pull/5454))
- Fix basic case of overlapping markers ([#5488](https://github.com/astral-sh/uv/pull/5488))

## 0.2.30

### Enhancements

- Infer missing `.exe` in Windows Python discovery ([#5456](https://github.com/astral-sh/uv/pull/5456))
- Make `--reinstall` imply `--refresh` ([#5425](https://github.com/astral-sh/uv/pull/5425))

### CLI

- Add `--no-config` to replace `--isolated` ([#5463](https://github.com/astral-sh/uv/pull/5463))
- Cache metadata for source tree dependencies ([#5423](https://github.com/astral-sh/uv/pull/5423))

### Bug fixes

- Avoid canonicalizing executables on Windows ([#5446](https://github.com/astral-sh/uv/pull/5446))
- Set standard permissions for temporary files ([#5457](https://github.com/astral-sh/uv/pull/5457))

### Preview features

- Allow distributions to be absent in deserialization ([#5453](https://github.com/astral-sh/uv/pull/5453))
- Merge identical forks ([#5405](https://github.com/astral-sh/uv/pull/5405))
- Minor consistency fixes for code blocks ([#5437](https://github.com/astral-sh/uv/pull/5437))
- Prefer "lockfile" to "lock file" ([#5427](https://github.com/astral-sh/uv/pull/5427))
- Update documentation sections ([#5452](https://github.com/astral-sh/uv/pull/5452))
- Use `sitecustomize.py` to implement environment layering ([#5462](https://github.com/astral-sh/uv/pull/5462))
- Use stripped variants by default in Python install ([#5451](https://github.com/astral-sh/uv/pull/5451))

## 0.2.29

### Enhancements

- Add `--ci` mode to `uv cache prune` ([#5391](https://github.com/astral-sh/uv/pull/5391))
- Display Python installation key for discovered interpreters ([#5365](https://github.com/astral-sh/uv/pull/5365))

### Bug fixes

- Allow symlinks to files in scripts directory ([#5380](https://github.com/astral-sh/uv/pull/5380))
- Always accept already-installed pre-releases ([#5419](https://github.com/astral-sh/uv/pull/5419))
- Validate successful metadata fetch for direct dependencies ([#5392](https://github.com/astral-sh/uv/pull/5392))

### Documentation

- Add warning to `--link-mode=symlink` documentation ([#5387](https://github.com/astral-sh/uv/pull/5387))

### Preview features

- Add PyPy finder ([#5337](https://github.com/astral-sh/uv/pull/5337))
- Add `uv init --virtual` ([#5396](https://github.com/astral-sh/uv/pull/5396))
- Allow `uv init` in unmanaged projects ([#5372](https://github.com/astral-sh/uv/pull/5372))
- Allow comments in `.python-version[s]` ([#5350](https://github.com/astral-sh/uv/pull/5350))
- Always show lock updates in `uv lock` ([#5413](https://github.com/astral-sh/uv/pull/5413))
- Improvements to the docs content ([#5426](https://github.com/astral-sh/uv/pull/5426))
- Fix blurring from nav title box shadow ([#5374](https://github.com/astral-sh/uv/pull/5374))
- Ignore Ctrl-C signals in `uv run` and `uv tool run` ([#5395](https://github.com/astral-sh/uv/pull/5395))
- Ignore hidden directories in workspace discovery ([#5408](https://github.com/astral-sh/uv/pull/5408))
- Increase padding between each nav section ([#5373](https://github.com/astral-sh/uv/pull/5373))
- Mark `--raw-sources` as conflicting with sources-specific
arguments ([#5378](https://github.com/astral-sh/uv/pull/5378))
- Omit empty uv.tool.dev-dependencies on `uv init` ([#5406](https://github.com/astral-sh/uv/pull/5406))
- Omit interpreter path during `uv venv` with managed Python ([#5311](https://github.com/astral-sh/uv/pull/5311))
- Omit interpreter path from output when using managed Python ([#5313](https://github.com/astral-sh/uv/pull/5313))
- Reject Git CLI arguments with non-Git sources ([#5377](https://github.com/astral-sh/uv/pull/5377))
- Retain dependency specifier in `uv add` with sources ([#5370](https://github.com/astral-sh/uv/pull/5370))
- Show additions and removals in `uv lock` updates ([#5410](https://github.com/astral-sh/uv/pull/5410))
- Skip 'Nothing to uninstall' message when removing dangling
environments ([#5382](https://github.com/astral-sh/uv/pull/5382))
- Support `requirements.txt` files in `uv tool install`
and `uv tool run` ([#5362](https://github.com/astral-sh/uv/pull/5362))
- Use env variables in Github Actions docs ([#5411](https://github.com/astral-sh/uv/pull/5411))
- Use logo in documentation ([#5421](https://github.com/astral-sh/uv/pull/5421))
- Warn on `requirements.txt`-provided arguments in `uv run` et al ([#5364](https://github.com/astral-sh/uv/pull/5364))

## 0.2.28

### Enhancements

- Output stable ordering to `requirements.txt` in universal mode ([#5334](https://github.com/astral-sh/uv/pull/5334))
- Allow symlinks with `--find-links` ([#5323](https://github.com/astral-sh/uv/pull/5323))
- Add support for variations of `pythonw.exe` ([#5259](https://github.com/astral-sh/uv/pull/5259))

### CLI

- Stylize `Requires-Python` consistently in CLI output ([#5304](https://github.com/astral-sh/uv/pull/5304))
- Add `--show-version-specifiers` to `tree` ([#5240](https://github.com/astral-sh/uv/pull/5240))

### Performance

- Avoid always rebuilding dynamic metadata ([#5206](https://github.com/astral-sh/uv/pull/5206))
- Avoid URL parsing when deserializing wheels ([#5235](https://github.com/astral-sh/uv/pull/5235))

### Bug fixes

- Avoid cache prune failure due to removed interpreter ([#5286](https://github.com/astral-sh/uv/pull/5286))
- Avoid including empty extras in resolution ([#5306](https://github.com/astral-sh/uv/pull/5306))
- If multiple indices contain the same version, use the first index ([#5288](https://github.com/astral-sh/uv/pull/5288))
- Include URLs on graph edges ([#5312](https://github.com/astral-sh/uv/pull/5312))
- Match wheel tags against `Requires-Python` major-minor ([#5289](https://github.com/astral-sh/uv/pull/5289))
- Remove Simple API cache files for alternative indexes
in `cache clean` ([#5353](https://github.com/astral-sh/uv/pull/5353))
- Remove extraneous `are` from wheel tag error messages ([#5303](https://github.com/astral-sh/uv/pull/5303))
- Allow conflicting pre-release strategies when forking ([#5150](https://github.com/astral-sh/uv/pull/5150))
- Use tag error rather than requires-python error for ABI filtering ([#5296](https://github.com/astral-sh/uv/pull/5296))

### Preview features

- Add `requires-python` to `uv init` ([#5322](https://github.com/astral-sh/uv/pull/5322))
- Add `uv add --no-editable` ([#5246](https://github.com/astral-sh/uv/pull/5246))
- Add constraint dependencies to pyproject.toml ([#5248](https://github.com/astral-sh/uv/pull/5248))
- Add support for requirements files in `uv run` ([#4973](https://github.com/astral-sh/uv/pull/4973))
- Avoid redundant members update in `uv init` ([#5321](https://github.com/astral-sh/uv/pull/5321))
- Create member `pyproject.toml` prior to workspace discovery ([#5317](https://github.com/astral-sh/uv/pull/5317))
- Fix `uv init .` ([#5330](https://github.com/astral-sh/uv/pull/5330))
- Fix `uv init` creation of a sub-package by path ([#5247](https://github.com/astral-sh/uv/pull/5247))
- Fix colors in `uv tool run` suggestion ([#5267](https://github.com/astral-sh/uv/pull/5267))
- Improve consistency of `tool` CLI ([#5326](https://github.com/astral-sh/uv/pull/5326))
- Make tool install robust to malformed receipts ([#5305](https://github.com/astral-sh/uv/pull/5305))
- Reduce spacing between nav items ([#5310](https://github.com/astral-sh/uv/pull/5310))
- Respect exclusions in `uv init` ([#5318](https://github.com/astral-sh/uv/pull/5318))
- Store resolution options in lockfile ([#5264](https://github.com/astral-sh/uv/pull/5264))
- Use backticks in project init message ([#5302](https://github.com/astral-sh/uv/pull/5302))
- Ignores workspace when `--isolated` flag is used in `uv init` ([#5290](https://github.com/astral-sh/uv/pull/5290))
- Normalize directory names in `uv init` ([#5292](https://github.com/astral-sh/uv/pull/5292))
- Avoid project discovery in `uv python pin` if `--isolated` is
provided ([#5354](https://github.com/astral-sh/uv/pull/5354))
- Show symbolic links in `uv python list` ([#5343](https://github.com/astral-sh/uv/pull/5343))
- Discover workspace from target path in `uv init` ([#5250](https://github.com/astral-sh/uv/pull/5250))
- Do not create nested workspace in `uv init` ([#5293](https://github.com/astral-sh/uv/pull/5293))

## 0.2.27

### Enhancements

- Add GraalPy support ([#5141](https://github.com/astral-sh/uv/pull/5141))
- Add a `--verify-hashes` hash-checking mode ([#4007](https://github.com/astral-sh/uv/pull/4007))
- Discover all `python3.x` executables in the `PATH` ([#5148](https://github.com/astral-sh/uv/pull/5148))
- Support `--link-mode=symlink` ([#5208](https://github.com/astral-sh/uv/pull/5208))
- Warn about unconstrained direct deps in lowest resolution ([#5142](https://github.com/astral-sh/uv/pull/5142))
- Log origin of version selection ([#5186](https://github.com/astral-sh/uv/pull/5186))
- Key hash policy on version, rather than package ([#5169](https://github.com/astral-sh/uv/pull/5169))

### CLI

- Make missing project table a tracing warning ([#5194](https://github.com/astral-sh/uv/pull/5194))
- Remove trailing period from user-facing messages ([#5218](https://github.com/astral-sh/uv/pull/5218))

### Bug fixes

- Make entrypoint writes atomic to avoid overwriting symlinks ([#5165](https://github.com/astral-sh/uv/pull/5165))
- Use `which`-retrieved path directly when spawning pager ([#5198](https://github.com/astral-sh/uv/pull/5198))
- Don't apply irrelevant constraints when validating site-packages ([#5231](https://github.com/astral-sh/uv/pull/5231))
- Respect local versions for all user requirements ([#5232](https://github.com/astral-sh/uv/pull/5232))

### Preview features

- Add `--frozen` to `uv add`, `uv remove`, and `uv tree` ([#5214](https://github.com/astral-sh/uv/pull/5214))
- Add `--locked` and `--frozen` to `uv run` CLI ([#5196](https://github.com/astral-sh/uv/pull/5196))
- Add `uv tool dir --bin` to show executable directory ([#5160](https://github.com/astral-sh/uv/pull/5160))
- Add `uv tool list --show-paths` to show install paths ([#5164](https://github.com/astral-sh/uv/pull/5164))
- Add color to `python pin` CLI ([#5215](https://github.com/astral-sh/uv/pull/5215))
- Added a way to inspect installation scripts on Powershell(
Windows) ([#5157](https://github.com/astral-sh/uv/pull/5157))
- Avoid TOCTOU errors in `.python-version` reads ([#5223](https://github.com/astral-sh/uv/pull/5223))
- Only show the Python installed on the system if `--python-preference only-system` is
specified ([#5219](https://github.com/astral-sh/uv/pull/5219))
- Check `python pin` compatibility with `Requires-Python` ([#4989](https://github.com/astral-sh/uv/pull/4989))
- Enforce hashes in lockfile install ([#5170](https://github.com/astral-sh/uv/pull/5170))
- Fix reference to `uv run` in `uv tree` CLI ([#5216](https://github.com/astral-sh/uv/pull/5216))
- Handle universal vs. fork markers with `ResolverMarkers` ([#5099](https://github.com/astral-sh/uv/pull/5099))
- Implement `uv init` ([#4791](https://github.com/astral-sh/uv/pull/4791))
- Make Python install robust to individual failures ([#5199](https://github.com/astral-sh/uv/pull/5199))
- Make registry hashes optional in the lockfile ([#5166](https://github.com/astral-sh/uv/pull/5166))
- Merge extras in lockfile ([#5181](https://github.com/astral-sh/uv/pull/5181))
- Move integration guide docs and edit Azure integration guide ([#5117](https://github.com/astral-sh/uv/pull/5117))
- Process completed Python installs and uninstalls as a stream ([#5203](https://github.com/astral-sh/uv/pull/5203))
- Skip invalid tools in `uv tool list` ([#5156](https://github.com/astral-sh/uv/pull/5156))
- Touch-ups to tools guide ([#5202](https://github.com/astral-sh/uv/pull/5202))
- Use +- install output for Python versions ([#5201](https://github.com/astral-sh/uv/pull/5201))
- Use display representation for download error ([#5173](https://github.com/astral-sh/uv/pull/5173))
- Use specialized error message for invalid Python install / uninstall
requests ([#5171](https://github.com/astral-sh/uv/pull/5171))
- Use the strongest hash in the lockfile ([#5167](https://github.com/astral-sh/uv/pull/5167))
- Write project guide ([#5195](https://github.com/astral-sh/uv/pull/5195))
- Write tools concept document ([#5207](https://github.com/astral-sh/uv/pull/5207))
- Fix reference to `projects.md` ([#5154](https://github.com/astral-sh/uv/pull/5154))
- Fixes to the settings documentation ([#5177](https://github.com/astral-sh/uv/pull/5177))
- Set exact version specifiers when resolving from lockfile ([#5193](https://github.com/astral-sh/uv/pull/5193))

## 0.2.26

### CLI

- Add `--no-progress` global option to hide all progress animations ([#5098](https://github.com/astral-sh/uv/pull/5098))

### Performance

- Cache downloaded wheel when range requests aren't supported ([#5089](https://github.com/astral-sh/uv/pull/5089))

### Bug fixes

- Download wheel to disk when streaming unzip failed with HTTP streaming
error ([#5094](https://github.com/astral-sh/uv/pull/5094))
- Filter out invalid wheels based on `requires-python` ([#5084](https://github.com/astral-sh/uv/pull/5084))
- Filter out none ABI wheels with mismatched Python versions ([#5087](https://github.com/astral-sh/uv/pull/5087))
- Lock Git cache on resolve ([#5051](https://github.com/astral-sh/uv/pull/5051))
- Change order of `pip compile` command checks to handle exact argument
first ([#5111](https://github.com/astral-sh/uv/pull/5111))

### Documentation

- Document that `--universal` implies `--no-strip-markers` ([#5121](https://github.com/astral-sh/uv/pull/5121))

### Preview features

- Indicate that `uv lock --upgrade` has updated the lock file ([#5110](https://github.com/astral-sh/uv/pull/5110))
- Sort managed Python installations by version ([#5140](https://github.com/astral-sh/uv/pull/5140))
- Support workspace to workspace path dependencies ([#4833](https://github.com/astral-sh/uv/pull/4833))
- Allow conflicting locals when forking ([#5104](https://github.com/astral-sh/uv/pull/5104))
- Rework `pyproject.toml` reformatting to respect original
indentation ([#5075](https://github.com/astral-sh/uv/pull/5075))

## 0.2.25

### Enhancements

- Include PyPy-specific executables when creating virtual environments
with `uv venv` ([#5047](https://github.com/astral-sh/uv/pull/5047))
- Add a custom error message for `--no-build-isolation` `torch`
dependencies ([#5041](https://github.com/astral-sh/uv/pull/5041))
- Improve missing `wheel` error message with `--no-build-isolation` ([#4964](https://github.com/astral-sh/uv/pull/4964))

### CLI

- Add `--no-pager` option in `help` command ([#5007](https://github.com/astral-sh/uv/pull/5007))
- Unhide `--isolated` global argument ([#5005](https://github.com/astral-sh/uv/pull/5005))
- Warn when unused `pyproject.toml` configuration is detected ([#5025](https://github.com/astral-sh/uv/pull/5025))

### Bug fixes

- Fall back to streaming wheel when `Content-Length` header is
absent ([#5000](https://github.com/astral-sh/uv/pull/5000))
- Fix substring marker expression disjointness checks ([#4998](https://github.com/astral-sh/uv/pull/4998))
- Lock directories to synchronize wheel-install copies ([#4978](https://github.com/astral-sh/uv/pull/4978))
- Normalize out complementary == or != markers ([#5050](https://github.com/astral-sh/uv/pull/5050))
- Retry on permission errors when persisting extracted source distributions to the
cache ([#5076](https://github.com/astral-sh/uv/pull/5076))
- Set absolute URLs prior to uploading to PyPI ([#5038](https://github.com/astral-sh/uv/pull/5038))
- Exclude `--upgrade-package` from the `pip compile` header ([#5032](https://github.com/astral-sh/uv/pull/5032))
- Exclude `--upgrade-package` when option and value are passed as a single
argument ([#5033](https://github.com/astral-sh/uv/pull/5033))
- Add split to cover marker universe when existing splits are
incomplete ([#5074](https://github.com/astral-sh/uv/pull/5074))
- Use correct `pyproject.toml` path in warnings ([#5069](https://github.com/astral-sh/uv/pull/5069))

### Documentation

- Fix `CONTRIBUTING.md` instructions to install multiple Python
versions ([#5015](https://github.com/astral-sh/uv/pull/5015))
- Use versioned badges when uploading to PyPI ([#5039](https://github.com/astral-sh/uv/pull/5039))

### Preview features

- Add documentation for running scripts ([#4968](https://github.com/astral-sh/uv/pull/4968))
- Add guide for tools ([#4982](https://github.com/astral-sh/uv/pull/4982))
- Allow URL dependencies in tool run `--from` ([#5002](https://github.com/astral-sh/uv/pull/5002))
- Add guide for authenticating to Azure Artifacts ([#4857](https://github.com/astral-sh/uv/pull/4857))
- Improve rc file detection based on rustup ([#5026](https://github.com/astral-sh/uv/pull/5026))
- Rename `python install --force` parameter to `--reinstall` ([#4999](https://github.com/astral-sh/uv/pull/4999))
- Use lockfile to prefill resolver index ([#4495](https://github.com/astral-sh/uv/pull/4495))
- `uv tool install` hint the correct when the executable is
available ([#5019](https://github.com/astral-sh/uv/pull/5019))
- `uv tool run` error messages references `uvx` when appropriate ([#5014](https://github.com/astral-sh/uv/pull/5014))
- `uvx` warns when requested executable is not provided by the
package [#5071](https://github.com/astral-sh/uv/pull/5071))
- Exit with zero when `uv tool install` request is already
satisfied ([#4986](https://github.com/astral-sh/uv/pull/4986))
- Respect the libc of the execution environment
with `uv python list` ([#5036](https://github.com/astral-sh/uv/pull/5036))
- Update standalone Pythons to include 3.12.4 ([#5042](https://github.com/astral-sh/uv/pull/5042))
- `uv tool run` suggest valid commands when command is not found ([#4997](https://github.com/astral-sh/uv/pull/4997))
- Add Windows path updates for `uv tool` ([#5029](https://github.com/astral-sh/uv/pull/5029))
- Add a command to append uv's binary directory to PATH ([#4975](https://github.com/astral-sh/uv/pull/4975))

## 0.2.24

### Enhancements

- Add support for 'any' Python requests ([#4948](https://github.com/astral-sh/uv/pull/4948))
- Allow constraints to be provided in `--upgrade-package` ([#4952](https://github.com/astral-sh/uv/pull/4952))
- Add `manylinux_2_31` to supported `--python-platform` ([#4965](https://github.com/astral-sh/uv/pull/4965))
- Improve marker simplification ([#4639](https://github.com/astral-sh/uv/pull/4639))

### CLI

- Display short help menu when `--help` is used ([#4772](https://github.com/astral-sh/uv/pull/4772))
- Allow `uv help` global options during `uv help` ([#4906](https://github.com/astral-sh/uv/pull/4906))
- Use paging for `uv help` display when available ([#4909](https://github.com/astral-sh/uv/pull/4909))

### Performance

- Switch to single threaded async runtime ([#4934](https://github.com/astral-sh/uv/pull/4934))

### Bug fixes

- Avoid AND-ing multi-term specifiers in marker normalization ([#4911](https://github.com/astral-sh/uv/pull/4911))
- Avoid inferring package name for GitHub Archives ([#4928](https://github.com/astral-sh/uv/pull/4928))
- Retry on connection reset network errors ([#4960](https://github.com/astral-sh/uv/pull/4960))
- Apply extra to overrides and constraints ([#4829](https://github.com/astral-sh/uv/pull/4829))

### Rust API

- Allow `uv` crate to be used as a library ([#4642](https://github.com/astral-sh/uv/pull/4642))

### Preview features

- Add Python installation guide ([#4942](https://github.com/astral-sh/uv/pull/4942))
- Add `uv python pin` ([#4950](https://github.com/astral-sh/uv/pull/4950))
- Add command-separation for Python discovery display ([#4916](https://github.com/astral-sh/uv/pull/4916))
- Avoid debug error for `uv run` with unknown Python version ([#4913](https://github.com/astral-sh/uv/pull/4913))
- Enable `--all` to uninstall all managed Pythons ([#4932](https://github.com/astral-sh/uv/pull/4932))
- Enable `--all` to uninstall all managed tools ([#4937](https://github.com/astral-sh/uv/pull/4937))
- Filter out markers based on Python requirement ([#4912](https://github.com/astral-sh/uv/pull/4912))
- Implement `uv tree` ([#4708](https://github.com/astral-sh/uv/pull/4708))
- Improve 'any' search message during `uv python install` ([#4940](https://github.com/astral-sh/uv/pull/4940))
- Lock for the duration of tool commands ([#4720](https://github.com/astral-sh/uv/pull/4720))
- Perform lock in `uv sync` by default ([#4839](https://github.com/astral-sh/uv/pull/4839))
- Reinstall and recreate environments when interpreter is removed ([#4935](https://github.com/astral-sh/uv/pull/4935))
- Respect `--isolated` in `uv python install` ([#4938](https://github.com/astral-sh/uv/pull/4938))
- Respect resolver settings in `uv remove` ([#4930](https://github.com/astral-sh/uv/pull/4930))
- Update "Python versions" documentation ([#4943](https://github.com/astral-sh/uv/pull/4943))
- Warn if tool binary directory is not on path ([#4951](https://github.com/astral-sh/uv/pull/4951))
- Avoid reparsing wheel URLs ([#4947](https://github.com/astral-sh/uv/pull/4947))
- Avoid serializing if lockfile does not change ([#4945](https://github.com/astral-sh/uv/pull/4945))

## 0.2.23

### Enhancements

- Update Windows trampoline binaries ([#4864](https://github.com/astral-sh/uv/pull/4864))
- Show user-facing warning when falling back to copy installs ([#4880](https://github.com/astral-sh/uv/pull/4880))

### Bug fixes

- Initialize all `--prefix` subdirectories ([#4895](https://github.com/astral-sh/uv/pull/4895))
- Respect `requires-python` when prefetching ([#4900](https://github.com/astral-sh/uv/pull/4900))
- Partially revert `Requires-Python` version narrowing ([#4902](https://github.com/astral-sh/uv/pull/4902))

### Preview features

- Avoid creating cache directories in tool directory ([#4868](https://github.com/astral-sh/uv/pull/4868))
- Add progress bar when downloading python ([#4840](https://github.com/astral-sh/uv/pull/4840))
- Add some decoration to tool CLI ([#4865](https://github.com/astral-sh/uv/pull/4865))
- Add some text decoration to toolchain CLI ([#4882](https://github.com/astral-sh/uv/pull/4882))
- Add user-facing output to indicate PEP 723 script ([#4881](https://github.com/astral-sh/uv/pull/4881))
- Ensure Pythons are aligned in `uv python list` ([#4884](https://github.com/astral-sh/uv/pull/4884))
- Fix always-plural message in uv python install ([#4866](https://github.com/astral-sh/uv/pull/4866))
- Skip installing `--with` requirements if present in base
environment ([#4879](https://github.com/astral-sh/uv/pull/4879))
- Sort dependencies before wheels and source distributions ([#4897](https://github.com/astral-sh/uv/pull/4897))
- Improve logging during resolver forking ([#4894](https://github.com/astral-sh/uv/pull/4894))

## 0.2.22

### CLI

- Add `--exclude-newer` to installer arguments ([#4785](https://github.com/astral-sh/uv/pull/4785))
- Bold durations in CLI messages ([#4818](https://github.com/astral-sh/uv/pull/4818))
- Drop crate description from the `uv` help menu ([#4773](https://github.com/astral-sh/uv/pull/4773))
- Update "about" in help menu ([#4782](https://github.com/astral-sh/uv/pull/4782))

### Configuration

- Add `UV_OVERRIDE` environment variable for `--override` ([#4836](https://github.com/astral-sh/uv/pull/4836))

### Bug fixes

- Always use release-only comparisons for `requires-python` ([#4794](https://github.com/astral-sh/uv/pull/4794))
- Avoid hangs before exiting CLI ([#4793](https://github.com/astral-sh/uv/pull/4793))
- Preserve verbatim URLs for `--find-links` ([#4838](https://github.com/astral-sh/uv/pull/4838))

### Preview features

- Always use base interpreter for cached environments ([#4805](https://github.com/astral-sh/uv/pull/4805))
- Cache tool environments in `uv tool run` ([#4784](https://github.com/astral-sh/uv/pull/4784))
- Check hash of downloaded python toolchain ([#4806](https://github.com/astral-sh/uv/pull/4806))
- Remove incompatible wheels from `uv.lock` ([#4799](https://github.com/astral-sh/uv/pull/4799))
- `uv cache prune` removes all cached environments ([#4845](https://github.com/astral-sh/uv/pull/4845))
- Add dedicated help menu for `uvx` ([#4770](https://github.com/astral-sh/uv/pull/4770))
- Change "toolchain" to "python" ([#4735](https://github.com/astral-sh/uv/pull/4735))
- Create empty environment for `uv run --isolated` ([#4849](https://github.com/astral-sh/uv/pull/4849))
- Deduplicate when install or uninstall python ([#4841](https://github.com/astral-sh/uv/pull/4841))
- Require at least one target for toolchain uninstalls ([#4820](https://github.com/astral-sh/uv/pull/4820))
- Resolve requirements prior to nuking tool environments ([#4788](https://github.com/astral-sh/uv/pull/4788))
- Tweak installation language in toolchain install ([#4811](https://github.com/astral-sh/uv/pull/4811))
- Use already-installed tools in `uv tool run` ([#4750](https://github.com/astral-sh/uv/pull/4750))
- Use cached environments in PEP 723 execution ([#4789](https://github.com/astral-sh/uv/pull/4789))
- Use optimized versions of managed Python on Linux ([#4775](https://github.com/astral-sh/uv/pull/4775))
- Fill Python requests with platform information during automatic
fetches ([#4810](https://github.com/astral-sh/uv/pull/4810))
- Remove installed python for force installation ([#4807](https://github.com/astral-sh/uv/pull/4807))
- Add tool version to list command ([#4674](https://github.com/astral-sh/uv/pull/4674))
- Add entrypoints to tool list ([#4661](https://github.com/astral-sh/uv/pull/4661))

## 0.2.21

- Fix issue where standalone installer failed to due missing `uvx.exe` binary on
Windows ([#4756](https://github.com/astral-sh/uv/pull/4756))

### CLI

- Differentiate `freeze` and `list` help text ([#4751](https://github.com/astral-sh/uv/pull/4751))

### Preview features

- Replace tool environments on updated Python request ([#4746](https://github.com/astral-sh/uv/pull/4746))

## 0.2.20

- Fix issue where the standalone installer failed due to a missing `uvx`
binary ([#4743](https://github.com/astral-sh/uv/pull/4743))

## 0.2.19

### Enhancements

- Indicate when we retried requests during network errors ([#4725](https://github.com/astral-sh/uv/pull/4725))

### CLI

- Add `--disable-pip-version-check` to compatibility arguments ([#4672](https://github.com/astral-sh/uv/pull/4672))
- Allow `uv pip sync` to clear an environment with opt-in ([#4517](https://github.com/astral-sh/uv/pull/4517))
- Add `--invert` to `uv pip tree` ([#4621](https://github.com/astral-sh/uv/pull/4621))
- Omit `(*)` in `uv pip tree` for empty packages ([#4673](https://github.com/astral-sh/uv/pull/4673))
- Add `--package` to `uv pip tree` ([#4655](https://github.com/astral-sh/uv/pull/4655))

### Bug fixes

- Fix bug where git cache did not validate commits correctly ([#4698](https://github.com/astral-sh/uv/pull/4698))
- Narrow `requires-python` requirement in resolver forks ([#4707](https://github.com/astral-sh/uv/pull/4707))
- Fix bug when pruning the last package in `uv pip tree` ([#4652](https://github.com/astral-sh/uv/pull/4652))

### Preview features

- Remove dangling environments in `uv tool uninstall` ([#4740](https://github.com/astral-sh/uv/pull/4740))
- Respect upgrades in `uv tool install` ([#4736](https://github.com/astral-sh/uv/pull/4736))
- Add PEP 723 support to `uv run` ([#4656](https://github.com/astral-sh/uv/pull/4656))
- Add `tool dir` and `toolchain dir` commands ([#4695](https://github.com/astral-sh/uv/pull/4695))
- Omit `pythonX.Y` segment in stdlib path for managed toolchains on
Windows ([#4727](https://github.com/astral-sh/uv/pull/4727))
- Add `uv toolchain uninstall` ([#4646](https://github.com/astral-sh/uv/pull/4646))
- Add `uvx` alias for `uv tool run` ([#4632](https://github.com/astral-sh/uv/pull/4632))
- Allow configuring the toolchain fetch strategy ([#4601](https://github.com/astral-sh/uv/pull/4601))
- Drop `prefer` prefix from `toolchain-preference` values ([#4602](https://github.com/astral-sh/uv/pull/4602))
- Enable projects to opt-out of workspace management ([#4565](https://github.com/astral-sh/uv/pull/4565))
- Fetch managed toolchains if necessary in `uv tool install`
and `uv tool run` ([#4717](https://github.com/astral-sh/uv/pull/4717))
- Fix tool dist-info directory normalization ([#4686](https://github.com/astral-sh/uv/pull/4686))
- Lock the toolchains directory during toolchain operations ([#4733](https://github.com/astral-sh/uv/pull/4733))
- Log when we start solving a fork ([#4684](https://github.com/astral-sh/uv/pull/4684))
- Reinstall entrypoints with `--force` ([#4697](https://github.com/astral-sh/uv/pull/4697))
- Respect data scripts in `uv tool install` ([#4693](https://github.com/astral-sh/uv/pull/4693))
- Set fork solution as preference when resolving ([#4662](https://github.com/astral-sh/uv/pull/4662))
- Show dedicated message for tools with no entrypoints ([#4694](https://github.com/astral-sh/uv/pull/4694))
- Support unnamed requirements in `uv tool install` ([#4716](https://github.com/astral-sh/uv/pull/4716))

## 0.2.18

### CLI

- Make `--universal` and `--python-platform` mutually exclusive ([#4598](https://github.com/astral-sh/uv/pull/4598))
- Add `--depth` and `--prune` support to `pip tree` ([#4440](https://github.com/astral-sh/uv/pull/4440))

### Bug fixes

- Handle cycles when propagating markers ([#4595](https://github.com/astral-sh/uv/pull/4595))
- Ignore `py` not found errors during interpreter discovery ([#4620](https://github.com/astral-sh/uv/pull/4620))
- Merge markers when applying constraints ([#4648](https://github.com/astral-sh/uv/pull/4648))
- Retry on spurious failures when caching built wheels ([#4605](https://github.com/astral-sh/uv/pull/4605))
- Sort indexes during graph edge removal ([#4649](https://github.com/astral-sh/uv/pull/4649))
- Treat Python version as a lower bound in `--universal` ([#4597](https://github.com/astral-sh/uv/pull/4597))
- Fix the incorrect handling of markers in `pip tree` ([#4611](https://github.com/astral-sh/uv/pull/4611))
- Improve toolchain and environment missing error messages ([#4596](https://github.com/astral-sh/uv/pull/4596))

### Documentation

- Explicitly mention use of seed packages during `uv venv --seed` ([#4588](https://github.com/astral-sh/uv/pull/4588))

### Preview features

- Add `uv tool list` ([#4630](https://github.com/astral-sh/uv/pull/4630))
- Add `uv tool uninstall` ([#4641](https://github.com/astral-sh/uv/pull/4641))
- Add support for specifying `name@version` in `uv tool run` ([#4572](https://github.com/astral-sh/uv/pull/4572))
- Allow `uv add` to specify optional dependency groups ([#4607](https://github.com/astral-sh/uv/pull/4607))
- Allow the package spec to be passed positionally in `uv tool install` ([#4564](https://github.com/astral-sh/uv/pull/4564))
- Avoid infinite loop for cyclic installs ([#4633](https://github.com/astral-sh/uv/pull/4633))
- Indent wheels like dependencies in the lockfile ([#4582](https://github.com/astral-sh/uv/pull/4582))
- Sync all packages in a virtual workspace ([#4636](https://github.com/astral-sh/uv/pull/4636))
- Use inline table for dependencies in lockfile ([#4581](https://github.com/astral-sh/uv/pull/4581))
- Make `source` field in lock file more structured ([#4627](https://github.com/astral-sh/uv/pull/4627))

## 0.2.17

### Bug fixes

- Avoid enforcing extra-only constraints ([#4570](https://github.com/astral-sh/uv/pull/4570))

### Preview features

- Add `--extra` to `uv add` and enable fine-grained updates ([#4566](https://github.com/astral-sh/uv/pull/4566))

## 0.2.16

### Enhancements

- Add a universal resolution mode to `uv pip compile`
with `--universal` ([#4505](https://github.com/astral-sh/uv/pull/4505))
- Add support for `--no-strip-markers` in `uv pip compile` output ([#4503](https://github.com/astral-sh/uv/pull/4503))
- Add `--no-dedupe` support to `uv pip tree` ([#4449](https://github.com/astral-sh/uv/pull/4449))

### Bug fixes

- Enable more precise environment locking with `--prefix` ([#4506](https://github.com/astral-sh/uv/pull/4506))
- Allow local index references in `requirements.txt` files ([#4525](https://github.com/astral-sh/uv/pull/4525))
- Allow non-`file://` paths to serve as `--index-url` values ([#4524](https://github.com/astral-sh/uv/pull/4524))
- Make `.egg-info` filename parsing spec compliant ([#4533](https://github.com/astral-sh/uv/pull/4533))
- Gracefully handle non-existent packages in local indexes ([#4545](https://github.com/astral-sh/uv/pull/4545))
- Read content length from response rather than request ([#4488](https://github.com/astral-sh/uv/pull/4488))
- Read persistent configuration from non-workspace `pyproject.toml` ([#4526](https://github.com/astral-sh/uv/pull/4526))
- Avoid panic for invalid, non-base index URLs ([#4527](https://github.com/astral-sh/uv/pull/4527))

### Performance

- Skip submodule update for fresh clones ([#4482](https://github.com/astral-sh/uv/pull/4482))
- Use shared client in Git fetch implementation ([#4487](https://github.com/astral-sh/uv/pull/4487))

### Preview features

- Add `--package` argument to `uv add` and `uv remove` ([#4556](https://github.com/astral-sh/uv/pull/4556))
- Add `uv tool install` ([#4492](https://github.com/astral-sh/uv/pull/4492))
- Fallback to interpreter discovery in `uv run` ([#4549](https://github.com/astral-sh/uv/pull/4549))
- Make `uv.sources` without `--preview` non-fatal ([#4558](https://github.com/astral-sh/uv/pull/4558))
- Remove non-existent extras from lockfile ([#4479](https://github.com/astral-sh/uv/pull/4479))
- Support conflicting URL in separate forks ([#4435](https://github.com/astral-sh/uv/pull/4435))
- Automatically detect workspace packages in `uv add` ([#4557](https://github.com/astral-sh/uv/pull/4557))
- Omit `distribution.sdist` from lockfile when it is redundant ([#4528](https://github.com/astral-sh/uv/pull/4528))
- Remove `source` and `version` from lock file when unambiguous ([#4513](https://github.com/astral-sh/uv/pull/4513))
- Allow `uv lock` to read overrides from `tool.uv` (#4108) ([#4369](https://github.com/astral-sh/uv/pull/4369))

## 0.2.15

### Enhancements

- Add `--emit-build-options` flag to `uv pip compile` interface ([#4463](https://github.com/astral-sh/uv/pull/4463))
- Add `pythonw` support for gui scripts on Windows ([#4409](https://github.com/astral-sh/uv/pull/4409))
- Add `uv pip tree` ([#3859](https://github.com/astral-sh/uv/pull/3859))

### CLI

- Adjust the docs for the pip CLI commands ([#4445](https://github.com/astral-sh/uv/pull/4445))
- Fix casing of `--no-compile` alias ([#4453](https://github.com/astral-sh/uv/pull/4453))

### Bug fixes

- Fix ordering of prefer-system toolchain preference ([#4441](https://github.com/astral-sh/uv/pull/4441))
- Respect index strategy in source distribution builds ([#4468](https://github.com/astral-sh/uv/pull/4468))

### Documentation

- Add documentation for using uv in a Docker image ([#4433](https://github.com/astral-sh/uv/pull/4433))

## 0.2.14

### Enhancements

- Support toolchain requests with platform-tag style Python implementations and
version ([#4407](https://github.com/astral-sh/uv/pull/4407))

### CLI

- Use "Prepared" instead of "Downloaded" in logs ([#4394](https://github.com/astral-sh/uv/pull/4394))

### Bug fixes

- Treat mismatched directory and file urls as unsatisfied
requirements ([#4393](https://github.com/astral-sh/uv/pull/4393))

### Preview features

- Expose `toolchain-preference` as a CLI and configuration file
option ([#4424](https://github.com/astral-sh/uv/pull/4424))
- Improve handling of command arguments in `uv run`
and `uv tool run` ([#4404](https://github.com/astral-sh/uv/pull/4404))
- Add `tool.uv.sources` support for `uv add` ([#4406](https://github.com/astral-sh/uv/pull/4406))
- Use correct lock path for workspace dependencies ([#4421](https://github.com/astral-sh/uv/pull/4421))
- Filter out sibling dependencies in resolver forks ([#4415](https://github.com/astral-sh/uv/pull/4415))

## 0.2.13

### Enhancements

- Add resolver tracing logs for when we filter requirements ([#4381](https://github.com/astral-sh/uv/pull/4381))

### Preview features

- Add `--workspace` option to `uv add` ([#4362](https://github.com/astral-sh/uv/pull/4362))
- Ignore query errors during `uv toolchain list` ([#4382](https://github.com/astral-sh/uv/pull/4382))
- Respect `.python-version` files and fetch managed toolchains in uv project
commands ([#4361](https://github.com/astral-sh/uv/pull/4361))
- Respect `.python-version` in `uv venv --preview` ([#4360](https://github.com/astral-sh/uv/pull/4360))

## 0.2.12

### Enhancements

- Allow specific `--only-binary` and `--no-binary` packages to
override `:all:` ([#4067](https://github.com/astral-sh/uv/pull/4067))
- Flatten ORs and ANDs in marker construction ([#4260](https://github.com/astral-sh/uv/pull/4260))
- Skip invalid interpreters when searching for requested interpreter executable
name ([#4308](https://github.com/astral-sh/uv/pull/4308))
- Display keyring stderr during queries ([#4343](https://github.com/astral-sh/uv/pull/4343))
- Allow discovery of uv binary relative to package root ([#4336](https://github.com/astral-sh/uv/pull/4336))
- Use relative path for `lib64` symlink ([#4268](https://github.com/astral-sh/uv/pull/4268))

### CLI

- Add uv version to debug output ([#4259](https://github.com/astral-sh/uv/pull/4259))
- Allow `--no-binary` with `uv pip compile` ([#4301](https://github.com/astral-sh/uv/pull/4301))
- Hide `--no-system` from the CLI ([#4292](https://github.com/astral-sh/uv/pull/4292))
- Make `--reinstall`, `--upgrade`, and `--refresh` shared arguments ([#4319](https://github.com/astral-sh/uv/pull/4319))

### Configuration

- Add `UV_EXCLUDE_NEWER` environment variable ([#4287](https://github.com/astral-sh/uv/pull/4287))

### Bug fixes

- Allow normalization to completely eliminate markers ([#4271](https://github.com/astral-sh/uv/pull/4271))
- Avoid treating direct path archives as always dynamic ([#4283](https://github.com/astral-sh/uv/pull/4283))
- De-duplicate markers during normalization ([#4263](https://github.com/astral-sh/uv/pull/4263))
- Fix incorrect parsing of requested Python version as empty version
specifiers ([#4289](https://github.com/astral-sh/uv/pull/4289))
- Suggest correct command to create a virtual environment when encountering externally managed
interpreters ([#4314](https://github.com/astral-sh/uv/pull/4314))
- Use consistent order for extra groups in lockfile ([#4275](https://github.com/astral-sh/uv/pull/4275))

### Documentation

- Add `pip-compile` defaults to `PIP_COMPATIBILITY.md` ([#4302](https://github.com/astral-sh/uv/pull/4302))
- Expand on `pip-compile` default differences ([#4306](https://github.com/astral-sh/uv/pull/4306))
- Tweak copy on some command-line arguments ([#4293](https://github.com/astral-sh/uv/pull/4293))
- Move the preview changelog so the GitHub Release shows stable
changes ([#4290](https://github.com/astral-sh/uv/pull/4290))

### Preview features

- Add `--force` option to `uv toolchain install` ([#4313](https://github.com/astral-sh/uv/pull/4313))
- Add `--no-build`, `--no-build-package`, and binary variants ([#4322](https://github.com/astral-sh/uv/pull/4322))
- Add `EXTERNALLY-MANAGED` markers to managed toolchains ([#4312](https://github.com/astral-sh/uv/pull/4312))
- Add `uv toolchain find` ([#4206](https://github.com/astral-sh/uv/pull/4206))
- Add persistent configuration for non-`pip` APIs ([#4294](https://github.com/astral-sh/uv/pull/4294))
- Add support for adding/removing development dependencies ([#4327](https://github.com/astral-sh/uv/pull/4327))
- Add support for listing system toolchains ([#4172](https://github.com/astral-sh/uv/pull/4172))
- Add support for toolchain requests by key ([#4332](https://github.com/astral-sh/uv/pull/4332))
- Allow multiple toolchains to be requested
in `uv toolchain install` ([#4334](https://github.com/astral-sh/uv/pull/4334))
- Fix relative and absolute path handling in lockfiles ([#4266](https://github.com/astral-sh/uv/pull/4266))
- Load configuration options from workspace root ([#4295](https://github.com/astral-sh/uv/pull/4295))
- Omit project name from workspace errors ([#4299](https://github.com/astral-sh/uv/pull/4299))
- Read Python version files during toolchain installs ([#4335](https://github.com/astral-sh/uv/pull/4335))
- Remove extraneous installations in `uv sync` by default ([#4366](https://github.com/astral-sh/uv/pull/4366))
- Respect `requires-python` in `uv lock` ([#4282](https://github.com/astral-sh/uv/pull/4282))
- Respect workspace-wide `requires-python` in interpreter selection ([#4298](https://github.com/astral-sh/uv/pull/4298))
- Support unnamed requirements in `uv add` ([#4326](https://github.com/astral-sh/uv/pull/4326))
- Use portable slash paths in lockfile ([#4324](https://github.com/astral-sh/uv/pull/4324))
- Use registry URL for fetching source distributions from lockfile ([#4280](https://github.com/astral-sh/uv/pull/4280))
- `uv sync --no-clean` ([#4367](https://github.com/astral-sh/uv/pull/4367))
- Filter dependencies by tracking markers on resolver forks ([#4339](https://github.com/astral-sh/uv/pull/4339))
- Use `Requires-Python` to filter dependencies during universal
resolution ([#4273](https://github.com/astral-sh/uv/pull/4273))

## 0.2.11

### Enhancements

- Add support for local directories with `--index-url` ([#4226](https://github.com/astral-sh/uv/pull/4226))
- Add mTLS support ([#4171](https://github.com/astral-sh/uv/pull/4171))
- Allow version specifiers to be used in Python version requests ([#4214](https://github.com/astral-sh/uv/pull/4214))

### Bug fixes

- Always install as editable when duplicate dependencies are
requested ([#4208](https://github.com/astral-sh/uv/pull/4208))
- Avoid crash with `XDG_CONFIG_HOME=/dev/null` ([#4200](https://github.com/astral-sh/uv/pull/4200))
- Improve handling of missing interpreters during discovery ([#4218](https://github.com/astral-sh/uv/pull/4218))
- Make missing `METADATA` file a recoverable error ([#4247](https://github.com/astral-sh/uv/pull/4247))
- Represent build tag as `u64` ([#4253](https://github.com/astral-sh/uv/pull/4253))

### Documentation

- Document Windows 10 requirement ([#4210](https://github.com/astral-sh/uv/pull/4210))

### Release

- Re-add `aarch64-unknown-linux-gnu` binary to release assets ([#4254](https://github.com/astral-sh/uv/pull/4254))

### Preview features

- Add changelog for preview changes ([#4251](https://github.com/astral-sh/uv/pull/4251))
- Allow direct URLs for dev dependencies ([#4233](https://github.com/astral-sh/uv/pull/4233))
- Create temporary environments in dedicated cache bucket ([#4223](https://github.com/astral-sh/uv/pull/4223))
- Improve output when an older toolchain version is already
installed ([#4248](https://github.com/astral-sh/uv/pull/4248))
- Initial implementation of `uv add` and `uv remove` ([#4193](https://github.com/astral-sh/uv/pull/4193))
- Refactor project interpreter request for `requires-python`
specifiers ([#4216](https://github.com/astral-sh/uv/pull/4216))
- Replace `toolchain fetch` with `toolchain install` ([#4228](https://github.com/astral-sh/uv/pull/4228))
- Support locking relative paths ([#4205](https://github.com/astral-sh/uv/pull/4205))
- Warn when 'requires-python' does not include a lower bound ([#4234](https://github.com/astral-sh/uv/pull/4234))

## 0.2.10

### Enhancements

- Accept `file://` URLs for `requirements.txt` et all references ([#4145](https://github.com/astral-sh/uv/pull/4145))
- Add support for `--prefix` ([#4085](https://github.com/astral-sh/uv/pull/4085))

### CLI

- Add `pyproject.toml` to CLI help ([#4181](https://github.com/astral-sh/uv/pull/4181))
- Drop "registry" prefix from request timeout log ([#4144](https://github.com/astral-sh/uv/pull/4144))

### Bug fixes

- Allow transitive URLs via recursive extras ([#4155](https://github.com/astral-sh/uv/pull/4155))
- Avoid pre-fetching for unbounded minimum versions ([#4149](https://github.com/astral-sh/uv/pull/4149))
- Avoid showing dev hints for Python requirements ([#4111](https://github.com/astral-sh/uv/pull/4111))
- Include non-standard ports in keyring host queries ([#4061](https://github.com/astral-sh/uv/pull/4061))
- Omit URL dependencies from pre-release hints ([#4140](https://github.com/astral-sh/uv/pull/4140))
- Improve static metadata extraction for Poetry projects ([#4182](https://github.com/astral-sh/uv/pull/4182))

### Documentation

- Document bytecode compilation in pip compatibility guide ([#4195](https://github.com/astral-sh/uv/pull/4195))
- Fix PEP 508 link in preview doc `specifying_dependencies` ([#4158](https://github.com/astral-sh/uv/pull/4158))
- Clarify role of `--system` flag ([#4031](https://github.com/astral-sh/uv/pull/4031))

### Preview features

- Add `uv toolchain install` ([#4164](https://github.com/astral-sh/uv/pull/4164))
- Add `uv toolchain list` ([#4163](https://github.com/astral-sh/uv/pull/4163))
- Add extra and dev dependency validation to lockfile ([#4112](https://github.com/astral-sh/uv/pull/4112))
- Add markers to edges rather than distributions ([#4166](https://github.com/astral-sh/uv/pull/4166))
- Cap `Requires-Python` comparisons at the patch version ([#4150](https://github.com/astral-sh/uv/pull/4150))
- Do not create a virtual environment when locking ([#4147](https://github.com/astral-sh/uv/pull/4147))
- Don't panic with invalid wheel source ([#4191](https://github.com/astral-sh/uv/pull/4191))
- Fetch managed toolchains in `uv run` ([#4143](https://github.com/astral-sh/uv/pull/4143))
- Fix PEP 508 link in preview doc `specifying_dependencies` ([#4158](https://github.com/astral-sh/uv/pull/4158))
- Ignore tags in universal resolution ([#4174](https://github.com/astral-sh/uv/pull/4174))
- Implement `Toolchain::find_or_fetch` and use
in `uv venv --preview` ([#4138](https://github.com/astral-sh/uv/pull/4138))
- Lock all packages in workspace ([#4016](https://github.com/astral-sh/uv/pull/4016))
- Recreate project environment if `--python` or `requires-python` doesn't
match ([#3945](https://github.com/astral-sh/uv/pull/3945))
- Respect `--find-links` in `lock` and `sync` ([#4183](https://github.com/astral-sh/uv/pull/4183))
- Set `--dev` to default for `uv run` and `uv sync` ([#4118](https://github.com/astral-sh/uv/pull/4118))
- Track `Markers` via a PubGrub package variant ([#4123](https://github.com/astral-sh/uv/pull/4123))
- Use union of `requires-python` in workspace ([#4041](https://github.com/astral-sh/uv/pull/4041))
- make universal resolver fork only when markers are disjoint ([#4135](https://github.com/astral-sh/uv/pull/4135))

## 0.2.9

### Enhancements

- Respect existing `.egg-link` files in site packages ([#4082](https://github.com/astral-sh/uv/pull/4082))

### Bug fixes

- Avoid extra-only filtering for constraints ([#4095](https://github.com/astral-sh/uv/pull/4095))

### Documentation

- Add install link for specific version to README ([#4105](https://github.com/astral-sh/uv/pull/4105))

### Preview features

- Add support for development dependencies ([#4036](https://github.com/astral-sh/uv/pull/4036))
- Avoid enforcing distribution ID uniqueness for extras ([#4104](https://github.com/astral-sh/uv/pull/4104))
- Ignore upper-bounds on `Requires-Python` ([#4086](https://github.com/astral-sh/uv/pull/4086))

## 0.2.8

### Bug fixes

- Fix `uv venv` handling when `VIRTUAL_ENV` refers to an non-existent
environment ([#4073](https://github.com/astral-sh/uv/pull/4073))

### Preview features

- Default to current Python minor if `Requires-Python` is absent ([#4070](https://github.com/astral-sh/uv/pull/4070))
- Enforce `Requires-Python` when syncing ([#4068](https://github.com/astral-sh/uv/pull/4068))
- Track supported Python range in lockfile ([#4065](https://github.com/astral-sh/uv/pull/4065))

## 0.2.7

### CLI

- Support `NO_COLOR` and `FORCE_COLOR` environment variables ([#3979](https://github.com/astral-sh/uv/pull/3979))

### Performance

- Avoid building packages with dynamic versions ([#4058](https://github.com/astral-sh/uv/pull/4058))
- Avoid work-stealing in bytecode compilation ([#4004](https://github.com/astral-sh/uv/pull/4004))

### Bug fixes

- Avoid dropping `pip sync` requirements with markers ([#4051](https://github.com/astral-sh/uv/pull/4051))
- Bias towards local directories for bare editable requirements ([#3995](https://github.com/astral-sh/uv/pull/3995))
- Preserve fragments when applying verbatim redirects ([#4038](https://github.com/astral-sh/uv/pull/4038))
- Avoid 'are incompatible' for singular bounded versions ([#4003](https://github.com/astral-sh/uv/pull/4003))

### Preview features

- Fix a bug where no warning is output when parsing of workspace settings
fails. ([#4014](https://github.com/astral-sh/uv/pull/4014))
- Normalize extras in lockfile ([#3958](https://github.com/astral-sh/uv/pull/3958))
- Respect `Requires-Python` in universal resolution ([#3998](https://github.com/astral-sh/uv/pull/3998))

## 0.2.6

### Enhancements

- Support PEP 508 requirements for editables ([#3946](https://github.com/astral-sh/uv/pull/3946))
- Discard fragments when parsing unnamed URLs ([#3940](https://github.com/astral-sh/uv/pull/3940))
- Port all Git functionality to use Git CLI ([#3833](https://github.com/astral-sh/uv/pull/3833))
- Use statically linked C runtime on Windows ([#3966](https://github.com/astral-sh/uv/pull/3966))

### Bug fixes

- Disable concurrent progress bars in Jupyter Notebooks ([#3890](https://github.com/astral-sh/uv/pull/3890))
- Initialize multi-progress state before individual bars ([#3901](https://github.com/astral-sh/uv/pull/3901))
- Add missing `i686` alias for `x86` ([#3899](https://github.com/astral-sh/uv/pull/3899))
- Add missing `ppc64le` alias for `powerpc64le` ([#3963](https://github.com/astral-sh/uv/pull/3963))
- Fix reference to `--python-version` patch behavior ([#3989](https://github.com/astral-sh/uv/pull/3989))
- Avoid race condition in `OnceMap` ([#3987](https://github.com/astral-sh/uv/pull/3987))

### Preview features

- Add `uv run --package` ([#3864](https://github.com/astral-sh/uv/pull/3864))
- Add index URL parameters to Project CLI ([#3984](https://github.com/astral-sh/uv/pull/3984))
- Avoid re-adding solutions to forked state ([#3967](https://github.com/astral-sh/uv/pull/3967))
- Draft for user docs for workspaces ([#3866](https://github.com/astral-sh/uv/pull/3866))
- Include all extras when generating lockfile ([#3912](https://github.com/astral-sh/uv/pull/3912))
- Remove unstable uv lock from pip interface ([#3970](https://github.com/astral-sh/uv/pull/3970))
- Respect resolved Git SHAs in `uv lock` ([#3956](https://github.com/astral-sh/uv/pull/3956))
- Use lockfile in `uv run` ([#3894](https://github.com/astral-sh/uv/pull/3894))
- Use lockfile versions as resolution preferences ([#3921](https://github.com/astral-sh/uv/pull/3921))
- Use universal resolution in `uv lock` ([#3969](https://github.com/astral-sh/uv/pull/3969))

## 0.2.5

### Enhancements

- Add support for x86 Windows ([#3873](https://github.com/astral-sh/uv/pull/3873))
- Add support for `prepare_metadata_for_build_editable` hook ([#3870](https://github.com/astral-sh/uv/pull/3870))
- Add concurrent progress bars for downloads ([#3252](https://github.com/astral-sh/uv/pull/3252))

### Bug fixes

- Update bundled Python URLs and add `"arm"` architecture variant ([#3855](https://github.com/astral-sh/uv/pull/3855))

### Preview features

- Add context to failed `uv tool run` ([#3882](https://github.com/astral-sh/uv/pull/3882))
- Add persistent storage of installed toolchains ([#3797](https://github.com/astral-sh/uv/pull/3797))
- Gate discovery of managed toolchains with preview ([#3835](https://github.com/astral-sh/uv/pull/3835))
- Initial workspace support ([#3705](https://github.com/astral-sh/uv/pull/3705))
- Move editable discovery behind `--preview` for now ([#3884](https://github.com/astral-sh/uv/pull/3884))

## 0.2.4

### CLI

- Allow `--system` and `--python` to be passed together ([#3830](https://github.com/astral-sh/uv/pull/3830))

### Bug fixes

- Ignore `libc` on other platforms ([#3825](https://github.com/astral-sh/uv/pull/3825))

## 0.2.3

### Enhancements

- Incorporate build tag into wheel prioritization ([#3781](https://github.com/astral-sh/uv/pull/3781))
- Avoid displaying log for satisfied editables if none are
requested ([#3795](https://github.com/astral-sh/uv/pull/3795))
- Improve logging during interpreter discovery ([#3790](https://github.com/astral-sh/uv/pull/3790))
- Improve logging for environment locking ([#3792](https://github.com/astral-sh/uv/pull/3792))
- Improve logging of interpreter implementation ([#3791](https://github.com/astral-sh/uv/pull/3791))
- Remove extra details from interpreter query traces ([#3803](https://github.com/astral-sh/uv/pull/3803))
- Use colon more consistently in error messages ([#3788](https://github.com/astral-sh/uv/pull/3788))

### Configuration

- Add JSON alias for `unsafe-any-match` ([#3820](https://github.com/astral-sh/uv/pull/3820))

### Release

- Remove redundant dynamically linked Linux binary again (#3762)" ([#3778](https://github.com/astral-sh/uv/pull/3778))
- Remove `aarch64-unknown-linux-gnu` from list of expected binaries ([#3761](https://github.com/astral-sh/uv/pull/3761))

### Bug fixes

- Always include package names for Git and HTTPS dependencies ([#3821](https://github.com/astral-sh/uv/pull/3821))
- Fix interpreter cache collisions for relative virtualenv paths ([#3823](https://github.com/astral-sh/uv/pull/3823))
- Ignore unnamed requirements in preferences ([#3826](https://github.com/astral-sh/uv/pull/3826))
- Search for `python3` in unix virtual environments ([#3798](https://github.com/astral-sh/uv/pull/3798))
- Use a cross-platform representation for relative paths
in `pip compile` ([#3804](https://github.com/astral-sh/uv/pull/3804))

### Preview features

- Allow specification of additional requirements in `uv tool run` ([#3678](https://github.com/astral-sh/uv/pull/3678))

## 0.2.2

### Enhancements

- Report yanks for cached and resolved packages ([#3772](https://github.com/astral-sh/uv/pull/3772))
- Improve error message when default Python is not found ([#3770](https://github.com/astral-sh/uv/pull/3770))

### Bug fixes

- Do not treat interpreters discovered via `CONDA_PREFIX` as system
interpreters ([#3771](https://github.com/astral-sh/uv/pull/3771))

## 0.2.1

### Bug fixes

- Re-added the dynamically-linked Linux binary ([#3762](https://github.com/astral-sh/uv/pull/3762))

### Preview features

- Allow users to specify a custom source package to `uv tool run` ([#3677](https://github.com/astral-sh/uv/pull/3677))

## 0.2.0

Starting with this release, uv will use the **minor** version tag to indicate breaking changes.

### Breaking

In this release, discovery of Python interpreters has changed. These changes should have a limited effect in most
use-cases, however, it has been marked as a breaking change because the interpreter used by uv could change in
some edge cases.

When multiple Python interpreters are installed, uv makes an attempt to find the exact version you requested.
Previously, uv would stop at the first Python interpreter it discovered — if the interpreter did not satisfy
the requested version, uv would fail. Now, uv will query multiple Python interpreters until it finds the
requested version, skipping interpreters that are broken or do not satisfy the request.

Additionally, uv now allows requests for interpreter implementations such as `pypy` and `cpython`. For example,
the request `--python cpython` will ignore a `python` executable that's implemented by `pypy`. These requests may
also include a version, e.g., `--python pypy@3.10`. By default, uv will accept *any* interpreter implementation.

In summary, the following Python interpreter requests are now allowed:

- A Python version without an implementation name, e.g., `3.10`
- A path to a directory containing a Python installation, e.g., `./foo/.venv`
- A path to a Python executable, e.g., `~/bin/python`
- A Python implementation without a version, e.g., `pypy` or `cpython`
- A Python implementation name and version, e.g., `pypy3.8` or `pypy@3.8`
- The name of a Python executable (for lookup in the `PATH`), e.g., `foopython3`

Previously, interpreter requests that were not versions or paths were always treated as executable
names.

To align the user expectations, uv now respects the interpreter that starts it. For example, `python -m uv ...` will
now prefer the `python` interpreter that was used to start uv instead of searching for a virtual environment.

We now check if discovered interpreters are virtual environments. This means that setting `VIRTUAL_ENV` to a Python
installation directory that is *not* a virtual environment will no longer work. Instead, use `--system`
or `--python <path>`
to request the interpreter.

### Enhancements

- Rewrite Python interpreter discovery ([#3266](https://github.com/astral-sh/uv/pull/3266))
- Add support for requesting `pypy` interpreters by implementation
name ([#3706](https://github.com/astral-sh/uv/pull/3706))
- Discover and prefer the parent interpreter when invoked
with `python -m uv` [#3736](https://github.com/astral-sh/uv/pull/3736)
- Add PEP 714 support for HTML API client ([#3697](https://github.com/astral-sh/uv/pull/3697))
- Add PEP 714 support for JSON API client ([#3698](https://github.com/astral-sh/uv/pull/3698))
- Write relative paths with unnamed requirement syntax ([#3682](https://github.com/astral-sh/uv/pull/3682))
- Allow relative Python executable paths in Windows trampoline ([#3717](https://github.com/astral-sh/uv/pull/3717))
- Add support for clang and msvc in missing header error ([#3753](https://github.com/astral-sh/uv/pull/3753))

### CLI

- Allow `--constraint` files in `pip sync` ([#3741](https://github.com/astral-sh/uv/pull/3741))
- Allow `--config-file` to be passed before or after command name ([#3730](https://github.com/astral-sh/uv/pull/3730))
- Make `--offline` a global argument ([#3729](https://github.com/astral-sh/uv/pull/3729))

### Performance

- Improve performance in complex resolutions by reducing cost of PubGrub package
clones ([#3688](https://github.com/astral-sh/uv/pull/3688))

### Bug fixes

- Evaluate arbitrary markers to `false` ([#3681](https://github.com/astral-sh/uv/pull/3681))
- Improve `DirWithoutEntrypoint` error message ([#3690](https://github.com/astral-sh/uv/pull/3690))
- Improve display of root package in range errors ([#3711](https://github.com/astral-sh/uv/pull/3711))
- Propagate URL errors in verbatim parsing ([#3720](https://github.com/astral-sh/uv/pull/3720))
- Report yanked packages in `--dry-run` ([#3740](https://github.com/astral-sh/uv/pull/3740))

### Release

- Drop native `manylinux` wheel in favor of dual-tagged wheel ([#3685](https://github.com/astral-sh/uv/pull/3685))
- The `python-patch` test feature is no longer on by default and must be manually enabled to test patch version
behavior ([#3746](https://github.com/astral-sh/uv/pull/3746))

### Documentation

- Add `--prefix` link to compatibility guide ([#3734](https://github.com/astral-sh/uv/pull/3734))
- Add `--only-binary` to compatibility guide ([#3735](https://github.com/astral-sh/uv/pull/3735))
- Add instructions for building and updating `uv-trampolines` ([#3731](https://github.com/astral-sh/uv/pull/3731))
- Add notes for testing on Windows ([#3658](https://github.com/astral-sh/uv/pull/3658))

### Preview features

- Add initial implementation of `uv tool run` ([#3657](https://github.com/astral-sh/uv/pull/3657))
- Add offline support to `uv tool run` and `uv run` ([#3676](https://github.com/astral-sh/uv/pull/3676))
- Better error message for `uv run` failures ([#3691](https://github.com/astral-sh/uv/pull/3691))
- Discover workspaces without using them in resolution ([#3585](https://github.com/astral-sh/uv/pull/3585))
- Support editables in `uv sync` ([#3692](https://github.com/astral-sh/uv/pull/3692))
- Track editable requirements in lockfile ([#3725](https://github.com/astral-sh/uv/pull/3725))

## 0.1.45

### Enhancements

- Parse and store extras on editable requirements ([#3629](https://github.com/astral-sh/uv/pull/3629))
- Allow local versions in wheel filenames ([#3596](https://github.com/astral-sh/uv/pull/3596))
- Create lib64 symlink for 64-bit, non-macOS, POSIX environments ([#3584](https://github.com/astral-sh/uv/pull/3584))

### Configuration

- Add `UV_CONCURRENT_INSTALLS` variable in favor
of `RAYON_NUM_THREADS` ([#3646](https://github.com/astral-sh/uv/pull/3646))
- Add serialization and deserialization for `--find-links` ([#3619](https://github.com/astral-sh/uv/pull/3619))
- Apply combination logic to merge CLI and persistent configuration ([#3618](https://github.com/astral-sh/uv/pull/3618))

### Performance

- Parallelize resolver ([#3627](https://github.com/astral-sh/uv/pull/3627))

### Bug fixes

- Reduce sensitivity of unknown option error to discard Python 2
interpreters ([#3580](https://github.com/astral-sh/uv/pull/3580))
- Respect installed packages in `uv run` ([#3603](https://github.com/astral-sh/uv/pull/3603))
- Separate cache construction from initialization ([#3607](https://github.com/astral-sh/uv/pull/3607))
- Add missing `"directory"` branch in source match ([#3608](https://github.com/astral-sh/uv/pull/3608))
- Fix source annotation in pip compile `annotation-style=line`
output ([#3637](https://github.com/astral-sh/uv/pull/3637))
- Run cargo update to pull in h2 ([#3638](https://github.com/astral-sh/uv/pull/3638))
- URL-decode hashes in HTML fragments ([#3655](https://github.com/astral-sh/uv/pull/3655))
- Always print JSON output with `--format` json ([#3671](https://github.com/astral-sh/uv/pull/3671))

### Documentation

- Add `UV_CONFIG_FILE` environment variable to documentation ([#3653](https://github.com/astral-sh/uv/pull/3653))
- Explicitly mention `--user` in compatibility guide ([#3666](https://github.com/astral-sh/uv/pull/3666))

### Release

- Add musl ppc64le support ([#3537](https://github.com/astral-sh/uv/pull/3537))
- Retag musl aarch64 for manylinux2014 ([#3624](https://github.com/astral-sh/uv/pull/3624))

### Preview features

- Add direct URL conversion to lockfile ([#3633](https://github.com/astral-sh/uv/pull/3633))
- Add hashes and versions to all distributions ([#3589](https://github.com/astral-sh/uv/pull/3589))
- Add local path conversions from lockfile ([#3609](https://github.com/astral-sh/uv/pull/3609))
- Add missing `"directory"` branch in source match ([#3608](https://github.com/astral-sh/uv/pull/3608))
- Add registry file size to lockfile ([#3652](https://github.com/astral-sh/uv/pull/3652))
- Add registry source distribution support to lockfile ([#3649](https://github.com/astral-sh/uv/pull/3649))
- Refactor editables for supporting them in bluejay commands ([#3639](https://github.com/astral-sh/uv/pull/3639))
- Rename `sourcedist` to `sdist` in lockfile ([#3590](https://github.com/astral-sh/uv/pull/3590))
- Respect installed packages in `uv run` ([#3603](https://github.com/astral-sh/uv/pull/3603))
- Support lossless serialization for Git dependencies in lockfile ([#3630](https://github.com/astral-sh/uv/pull/3630))

## 0.1.44

### Release

Reverts "Use manylinux: auto to enable `musllinux_1_2` aarch64
builds ([#3444](https://github.com/astral-sh/uv/pull/3444))"

The manylinux change appeared to introduce SSL errors when building aarch64 Docker images, e.g.,

> invalid peer certificate: BadSignature

The v0.1.42 behavior for aarch64 manylinux builds is restored in this release.

See [#3576](https://github.com/astral-sh/uv/pull/3576)

## 0.1.43

### Enhancements

- Annotate sources of requirements in `pip compile` output ([#3269](https://github.com/astral-sh/uv/pull/3269))
- Track origin for `setup.py` files and friends ([#3481](https://github.com/astral-sh/uv/pull/3481))

### Configuration

- Consolidate concurrency limits and expose as environment
variables ([#3493](https://github.com/astral-sh/uv/pull/3493))

### Release

- Use manylinux: auto to enable `musllinux_1_2` aarch64 builds ([#3444](https://github.com/astral-sh/uv/pull/3444))
- Enable musllinux_1_1 wheels ([#3523](https://github.com/astral-sh/uv/pull/3523))

### Bug fixes

- Avoid keyword arguments for PEP 517 build hooks ([#3517](https://github.com/astral-sh/uv/pull/3517))
- Apply advisory locks when building source distributions ([#3525](https://github.com/astral-sh/uv/pull/3525))
- Avoid attempting to build editables when fetching metadata ([#3563](https://github.com/astral-sh/uv/pull/3563))
- Clone individual files on windows ReFS ([#3551](https://github.com/astral-sh/uv/pull/3551))
- Filter irrelevant requirements from source annotations ([#3479](https://github.com/astral-sh/uv/pull/3479))
- Make cache clearing robust to directories without read
permissions ([#3524](https://github.com/astral-sh/uv/pull/3524))
- Respect constraints on editable dependencies ([#3554](https://github.com/astral-sh/uv/pull/3554))
- Skip Python 2 versions when locating Python ([#3476](https://github.com/astral-sh/uv/pull/3476))
- Make `--isolated` a global argument ([#3558](https://github.com/astral-sh/uv/pull/3558))
- Allow unknown `pyproject.toml` fields ([#3511](https://github.com/astral-sh/uv/pull/3511))
- Change error value detection for glibc ([#3487](https://github.com/astral-sh/uv/pull/3487))

### Preview features

- Create virtualenv if it doesn't exist in project API ([#3499](https://github.com/astral-sh/uv/pull/3499))
- Discover `uv run` projects hierarchically ([#3494](https://github.com/astral-sh/uv/pull/3494))
- Read and write `uv.lock` based on project root ([#3497](https://github.com/astral-sh/uv/pull/3497))
- Read package name from `pyproject.toml` in `uv run` ([#3496](https://github.com/astral-sh/uv/pull/3496))
- Rebrand workspace API as project API ([#3489](https://github.com/astral-sh/uv/pull/3489))

## 0.1.42

This release includes stabilized support for persistent configuration in uv.

uv will now read project configuration from a `pyproject.toml` or `uv.toml` file in the current
directory or any parent directory, along with user configuration at `~/.config/uv/uv.toml`
(or `$XDG_CONFIG_HOME/uv/uv.toml`) on macOS and Linux, and `%APPDATA%\uv\uv.toml` on Windows.

See: [Persistent Configuration](https://github.com/astral-sh/uv?tab=readme-ov-file#persistent-configuration) for more.

### Enhancements

- Respect `MACOSX_DEPLOYMENT_TARGET` in `--python-platform` ([#3470](https://github.com/astral-sh/uv/pull/3470))

### Configuration

- Add documentation for persistent configuration ([#3467](https://github.com/astral-sh/uv/pull/3467))
- Add JSON Schema export to SchemaStore ([#3461](https://github.com/astral-sh/uv/pull/3461))
- Merge user and workspace settings ([#3462](https://github.com/astral-sh/uv/pull/3462))

### Bug fixes

- Use Metadata10 to parse PKG-INFO of legacy editable ([#3450](https://github.com/astral-sh/uv/pull/3450))
- Apply normcase to line from easy-install.pth ([#3451](https://github.com/astral-sh/uv/pull/3451))
- Upgrade `async_http_range_reader` to v0.8.0 to respect redirects in range
requests ([#3460](https://github.com/astral-sh/uv/pull/3460))
- Use last non-EOL version for `--python-platform` macOS ([#3469](https://github.com/astral-sh/uv/pull/3469))

### Preview features

- Use environment layering for `uv run --with` ([#3447](https://github.com/astral-sh/uv/pull/3447))
- Warn when missing minimal bounds when using `tool.uv.sources` ([#3452](https://github.com/astral-sh/uv/pull/3452))

## 0.1.41

### Bug fixes

- Remove unconstrained version error from requirements ([#3443](https://github.com/astral-sh/uv/pull/3443))

## 0.1.40

### Enhancements

- Add `--allow-existing` to overwrite existing virtualenv ([#2548](https://github.com/astral-sh/uv/pull/2548))
- Respect and enable uninstalls of legacy editables (`.egg-link`) ([#3415](https://github.com/astral-sh/uv/pull/3415))
- Respect and enable uninstalls of existing `.egg-info` packages ([#3380](https://github.com/astral-sh/uv/pull/3380))

### CLI

- Accept `--no-upgrade`, `--no-refresh`, etc. on the CLI ([#3328](https://github.com/astral-sh/uv/pull/3328))

### Configuration

- Expose `UV_NO_BUILD_ISOLATION` as environment variable ([#3318](https://github.com/astral-sh/uv/pull/3318))
- Expose `UV_PYTHON` as an environment variable ([#3284](https://github.com/astral-sh/uv/pull/3284))
- Expose `UV_LINK_MODE` as environment variable ([#3315](https://github.com/astral-sh/uv/pull/3315))
- Add `UV_CUSTOM_COMPILE_COMMAND` to environment variable docs ([#3382](https://github.com/astral-sh/uv/pull/3382))

### Bug fixes

- Ignore 401 HTTP responses with multiple indexes ([#3292](https://github.com/astral-sh/uv/pull/3292))
- Avoid panic for file URLs ([#3306](https://github.com/astral-sh/uv/pull/3306))
- Quote version parse errors consistently ([#3325](https://github.com/astral-sh/uv/pull/3325))
- Detect current environment when `uv` is invoked from within a
virtualenv ([#3379](https://github.com/astral-sh/uv/pull/3379))
- Unset target when creating virtual environments ([#3362](https://github.com/astral-sh/uv/pull/3362))
- Update activation scripts from virtualenv ([#3376](https://github.com/astral-sh/uv/pull/3376))
- Use canonical URLs in satisfaction check ([#3373](https://github.com/astral-sh/uv/pull/3373))

### Preview features

- Add basic `tool.uv.sources` support ([#3263](https://github.com/astral-sh/uv/pull/3263))
- Improve non-git error message ([#3403](https://github.com/astral-sh/uv/pull/3403))
- Preserve given for `tool.uv.sources` paths ([#3412](https://github.com/astral-sh/uv/pull/3412))
- Restore verbatim in error message ([#3402](https://github.com/astral-sh/uv/pull/3402))
- Use preview mode for tool.uv.sources ([#3277](https://github.com/astral-sh/uv/pull/3277))
- Use top-level `--isolated` for `uv run` ([#3431](https://github.com/astral-sh/uv/pull/3431))
- add basic "install from lock file" operation ([#3340](https://github.com/astral-sh/uv/pull/3340))
- uv-resolver: add initial version of universal lock file format ([#3314](https://github.com/astral-sh/uv/pull/3314))

## 0.1.39

### Enhancements

- Add `--target` support to `sync` and `install` ([#3257](https://github.com/astral-sh/uv/pull/3257))
- Implement `--index-strategy unsafe-best-match` ([#3138](https://github.com/astral-sh/uv/pull/3138))

### Bug fixes

- Fix `platform_machine` tag for `--python-platform` on macOS ARM ([#3267](https://github.com/astral-sh/uv/pull/3267))

### Release

- Build a separate ARM wheel for macOS ([#3268](https://github.com/astral-sh/uv/pull/3268))
- Use `macos-12` to build release wheels ([#3264](https://github.com/astral-sh/uv/pull/3264))

## 0.1.38

### Enhancements

- Add alternate manylinux targets to `--python-platform` ([#3229](https://github.com/astral-sh/uv/pull/3229))
- An enum and backticks for lookahead error ([#3216](https://github.com/astral-sh/uv/pull/3216))
- Upgrade macOS target to `12.0` ([#3228](https://github.com/astral-sh/uv/pull/3228))
- Add keyring logs for URL and host fetches ([#3212](https://github.com/astral-sh/uv/pull/3212))
- Combine unresolvable error dependency clauses with the same root ([#3225](https://github.com/astral-sh/uv/pull/3225))

### CLI

- Gave a better name to the `--color` placeholder ([#3226](https://github.com/astral-sh/uv/pull/3226))
- Warn when an unsupported Python version is encountered ([#3250](https://github.com/astral-sh/uv/pull/3250))

### Configuration

- Use directory instead of file when searching for `uv.toml` file ([#3203](https://github.com/astral-sh/uv/pull/3203))

### Performance

- Only perform fetches of credentials for a realm and username combination
once ([#3237](https://github.com/astral-sh/uv/pull/3237))
- Unroll self-dependencies via extras ([#3230](https://github.com/astral-sh/uv/pull/3230))
- Use read-write locks instead of mutexes in authentication
handling ([#3210](https://github.com/astral-sh/uv/pull/3210))

### Bug fixes

- Avoid removing quotes from requirements markers ([#3214](https://github.com/astral-sh/uv/pull/3214))
- Avoid adding extras when expanding constraints ([#3232](https://github.com/astral-sh/uv/pull/3232))
- Reinstall package when editable label is removed ([#3219](https://github.com/astral-sh/uv/pull/3219))

### Documentation

- Add `RAYON_NUM_THREADS` to environment variable docs ([#3223](https://github.com/astral-sh/uv/pull/3223))
- Document support for HTTP proxy variables ([#3247](https://github.com/astral-sh/uv/pull/3247))
- Fix documentation for `--python-platform` ([#3220](https://github.com/astral-sh/uv/pull/3220))

## 0.1.37

### Enhancements

- Change default HTTP read timeout to 30s ([#3182](https://github.com/astral-sh/uv/pull/3182))
- Add `--python-platform` to `sync` and `install` commands ([#3154](https://github.com/astral-sh/uv/pull/3154))
- Add ticks around error messages more consistently ([#3004](https://github.com/astral-sh/uv/pull/3004))
- Fix Docker publish permissions in release pipeline ([#3195](https://github.com/astral-sh/uv/pull/3195))
- Improve tracing for keyring provider ([#3207](https://github.com/astral-sh/uv/pull/3207))

### Performance

- Update keyring provider to be async ([#3089](https://github.com/astral-sh/uv/pull/3089))

### Bug fixes

- Fix fetch of credentials when cache is seeded with username ([#3206](https://github.com/astral-sh/uv/pull/3206))

### Documentation

- Improve `--python-platform` documentation ([#3202](https://github.com/astral-sh/uv/pull/3202))

## 0.1.36

### Enhancements

- Add support for embedded Python on Windows ([#3161](https://github.com/astral-sh/uv/pull/3161))
- Add Docker image publishing to release pipeline ([#3155](https://github.com/astral-sh/uv/pull/3155))

### Configuration

- Add `UV_CONSTRAINT` environment variable to provide value
for `--constraint` ([#3162](https://github.com/astral-sh/uv/pull/3162))

### Bug fixes

- Avoid waiting for metadata for `--no-deps` editables ([#3188](https://github.com/astral-sh/uv/pull/3188))
- Fix `venvlauncher.exe` reference in venv creation ([#3160](https://github.com/astral-sh/uv/pull/3160))
- Fix authentication for URLs with a shared realm ([#3130](https://github.com/astral-sh/uv/pull/3130))
- Restrict observed requirements to direct when `--no-deps` is
specified ([#3191](https://github.com/astral-sh/uv/pull/3191))

### Documentation

- Add a versioning policy to the README ([#3151](https://github.com/astral-sh/uv/pull/3151))

## 0.1.35

### Enhancements

- Add a `--python-platform` argument to enable resolving against a target
platform ([#3111](https://github.com/astral-sh/uv/pull/3111))
- Enforce HTTP timeouts on a per-read (rather than per-request)
basis ([#3144](https://github.com/astral-sh/uv/pull/3144))

### Bug fixes

- Avoid preferring constrained over unconstrained packages ([#3148](https://github.com/astral-sh/uv/pull/3148))
- Allow `UV_SYSTEM_PYTHON=1` in addition to `UV_SYSTEM_PYTHON=true` ([#3136](https://github.com/astral-sh/uv/pull/3136))

## 0.1.34

### CLI

- Allow `--python` and `--system` on `pip compile` ([#3115](https://github.com/astral-sh/uv/pull/3115))
- Remove `Option<bool>` for `--no-cache` ([#3129](https://github.com/astral-sh/uv/pull/3129))
- Rename `--compile` to `--compile-bytecode` ([#3102](https://github.com/astral-sh/uv/pull/3102))
- Accept `0`, `1`, and similar values for Boolean environment
variables ([#3113](https://github.com/astral-sh/uv/pull/3113))

### Configuration

- Add `UV_REQUIRE_HASHES` environment variable ([#3125](https://github.com/astral-sh/uv/pull/3125))
- Add negation flags to the CLI ([#3050](https://github.com/astral-sh/uv/pull/3050))

### Bug fixes

- Avoid fetching unnecessary extra versions during resolution ([#3100](https://github.com/astral-sh/uv/pull/3100))
- Avoid deprioritizing recursive editables ([#3133](https://github.com/astral-sh/uv/pull/3133))
- Avoid treating localhost URLs as local file paths ([#3132](https://github.com/astral-sh/uv/pull/3132))
- Hide password in the index printed via `--emit-index-annotation` ([#3112](https://github.com/astral-sh/uv/pull/3112))
- Restore seeding of authentication cache from index URLs ([#3124](https://github.com/astral-sh/uv/pull/3124))

## 0.1.33

### Breaking changes

Using the keyring requires a username to be provided on index URLs now. Previously, the username `oauth2accesstoken`
was assumed. This will affect Google Artifact Registry users using `--keyring-provider subprocess` and an index URL
without a username. The suggested fix is to add the required username to index URLs,
e.g., `https://oauth2accesstoken@<url>`.

See [#2976](https://github.com/astral-sh/uv/pull/2976#discussion_r1566521453) for details.

### Enhancements

- Allow passing a virtual environment path to `uv pip --python` ([#3064](https://github.com/astral-sh/uv/pull/3064))
- Add compatibility argument for `pip list --outdated` ([#3055](https://github.com/astral-sh/uv/pull/3055))

### CLI

- Enable auto-wrapping of `--help` output ([#3058](https://github.com/astral-sh/uv/pull/3058))
- Show `--require-hashes` CLI argument in help ([#3093](https://github.com/astral-sh/uv/pull/3093))

### Performance

- Incorporate heuristics to improve package prioritization ([#3087](https://github.com/astral-sh/uv/pull/3087))

### Bug fixes

- Fix HTTP authentication when the password includes percent encoded characters (e.g. with Google Artifact
Registry) ([#2822](https://github.com/astral-sh/uv/issues/2822))
- Use usernames from URLs when looking for credentials in netrc files and the
keyring [#2563](https://github.com/astral-sh/uv/issues/2563))
- Skip `HEAD` requests for indexes that return 403 (e.g. PyPICloud) ([#3070](https://github.com/astral-sh/uv/pull/3070))
- Use kebab-case consistently ([#3080](https://github.com/astral-sh/uv/pull/3080))
- Show package name in no version for direct dependency error ([#3056](https://github.com/astral-sh/uv/pull/3056))
- Avoid erroring when encountering `.tar.bz2` source distributions ([#3069](https://github.com/astral-sh/uv/pull/3069))

## 0.1.32

### Enhancements

- Add a `--require-hashes` command-line setting ([#2824](https://github.com/astral-sh/uv/pull/2824))
- Add hash-checking support to `install` and `sync` ([#2945](https://github.com/astral-sh/uv/pull/2945))
- Add support for URL requirements in `--generate-hashes` ([#2952](https://github.com/astral-sh/uv/pull/2952))
- Allow unnamed requirements for overrides ([#2999](https://github.com/astral-sh/uv/pull/2999))
- Enforce and backtrack on invalid versions in source metadata ([#2954](https://github.com/astral-sh/uv/pull/2954))
- Fall back to distributions without hashes in resolver ([#2949](https://github.com/astral-sh/uv/pull/2949))
- Implement `--emit-index-annotation` to annotate source index for each
package ([#2926](https://github.com/astral-sh/uv/pull/2926))
- Log hard-link failures ([#3015](https://github.com/astral-sh/uv/pull/3015))
- Support free-threaded Python ([#2805](https://github.com/astral-sh/uv/pull/2805))
- Support unnamed requirements in `--require-hashes` ([#2993](https://github.com/astral-sh/uv/pull/2993))
- Respect link mode for builds, in `uv pip compile` and for `uv venv` seed
packages ([#3016](https://github.com/astral-sh/uv/pull/3016))
- Force color for build error messages ([#3032](https://github.com/astral-sh/uv/pull/3032))
- Surface invalid metadata as hints in error reports ([#2850](https://github.com/astral-sh/uv/pull/2850))

### Configuration

- Add `UV_BREAK_SYSTEM_PACKAGES` environment variable ([#2995](https://github.com/astral-sh/uv/pull/2995))

### CLI

- Remove some restrictions in argument groups ([#3001](https://github.com/astral-sh/uv/pull/3001))

### Bug fixes

- Add `--find-links` source distributions to the registry cache ([#2986](https://github.com/astral-sh/uv/pull/2986))
- Allow comments after all `requirements.txt` entries ([#3018](https://github.com/astral-sh/uv/pull/3018))
- Avoid cache invalidation on credentials renewal ([#3010](https://github.com/astral-sh/uv/pull/3010))
- Avoid calling `normalize_path` with relative paths that extend beyond the current
directory ([#3013](https://github.com/astral-sh/uv/pull/3013))
- Deduplicate symbolic links between `purelib` and `platlib` ([#3002](https://github.com/astral-sh/uv/pull/3002))
- Remove unused `--output-file` from `pip install` ([#2975](https://github.com/astral-sh/uv/pull/2975))
- Strip query string when parsing filename from HTML index ([#2961](https://github.com/astral-sh/uv/pull/2961))
- Update hashes without `--upgrade` if not present ([#2966](https://github.com/astral-sh/uv/pull/2966))

## 0.1.31

### Bug fixes

- Ignore direct URL distributions in prefetcher ([#2943](https://github.com/astral-sh/uv/pull/2943))

## 0.1.30

### Enhancements

- Show resolution diagnostics after `pip install` ([#2829](https://github.com/astral-sh/uv/pull/2829))

### Performance

- Speed up cold-cache `urllib3`-`boto3`-`botocore` performance with batched
prefetching ([#2452](https://github.com/astral-sh/uv/pull/2452))

### Bug fixes

- Backtrack on distributions with invalid metadata ([#2834](https://github.com/astral-sh/uv/pull/2834))
- Include LICENSE files in source distribution ([#2855](https://github.com/astral-sh/uv/pull/2855))
- Respect `--no-build` and `--no-binary` in `--find-links` ([#2826](https://github.com/astral-sh/uv/pull/2826))
- Respect cached local `--find-links` in install plan ([#2907](https://github.com/astral-sh/uv/pull/2907))
- Avoid panic with multiple confirmation handlers ([#2903](https://github.com/astral-sh/uv/pull/2903))
- Use scheme parsing to determine absolute vs. relative URLs ([#2904](https://github.com/astral-sh/uv/pull/2904))
- Remove additional 'because' in resolution failure messages ([#2849](https://github.com/astral-sh/uv/pull/2849))
- Use `miette` when printing `pip sync` resolution failures ([#2848](https://github.com/astral-sh/uv/pull/2848))

## 0.1.29

### Enhancements

- Allow conflicting Git URLs that refer to the same commit SHA ([#2769](https://github.com/astral-sh/uv/pull/2769))
- Allow package lookups across multiple indexes via explicit
opt-in (`--index-strategy unsafe-any-match`) ([#2815](https://github.com/astral-sh/uv/pull/2815))
- Allow no-op `--no-compile` flag on CLI ([#2816](https://github.com/astral-sh/uv/pull/2816))
- Upgrade `rs-async-zip` to support data descriptors ([#2809](https://github.com/astral-sh/uv/pull/2809))

### Bug fixes

- Avoid unused extras check in `pip install` for source trees ([#2811](https://github.com/astral-sh/uv/pull/2811))
- Deduplicate editables during install commands ([#2820](https://github.com/astral-sh/uv/pull/2820))
- Fix windows lock race: lock exclusive after all try lock errors ([#2800](https://github.com/astral-sh/uv/pull/2800))
- Preserve `.git` suffixes and casing in Git dependencies ([#2789](https://github.com/astral-sh/uv/pull/2789))
- Respect Git tags and branches that look like short commits ([#2795](https://github.com/astral-sh/uv/pull/2795))
- Enable virtualenv creation on Windows with cpython-x86 ([#2707](https://github.com/astral-sh/uv/pull/2707))

### Documentation

- Document that uv is safe to run concurrently ([#2818](https://github.com/astral-sh/uv/pull/2818))

## 0.1.28

### Enhancements

- Recursively resolve direct URL references upfront ([#2684](https://github.com/astral-sh/uv/pull/2684))

### Performance

- Populate the in-memory index when resolving lookahead URLs ([#2761](https://github.com/astral-sh/uv/pull/2761))

### Bug fixes

- Detect Fish via `FISH_VERSION` ([#2781](https://github.com/astral-sh/uv/pull/2781))
- Exclude installed distributions with multiple versions from consideration in the
resolver ([#2779](https://github.com/astral-sh/uv/pull/2779))
- Resolve non-deterministic behavior in preferences due to site-packages
ordering ([#2780](https://github.com/astral-sh/uv/pull/2780))
- Use canonical URL to key redirect map ([#2764](https://github.com/astral-sh/uv/pull/2764))
- Use distribution database and index for all pre-resolution phases ([#2766](https://github.com/astral-sh/uv/pull/2766))
- Fix `uv self update` on Linux ([#2783](https://github.com/astral-sh/uv/pull/2783))

## 0.1.27

### Enhancements

- Add `--exclude-editable` support to `pip-freeze` ([#2740](https://github.com/astral-sh/uv/pull/2740))
- Add `pyproject.toml` et al to list of prompted packages ([#2746](https://github.com/astral-sh/uv/pull/2746))
- Consider installed packages during resolution ([#2596](https://github.com/astral-sh/uv/pull/2596))
- Recursively allow URL requirements for local dependencies ([#2702](https://github.com/astral-sh/uv/pull/2702))

### Configuration

- Add `UV_RESOLUTION` environment variable for `--resolution` ([#2720](https://github.com/astral-sh/uv/pull/2720))

### Bug fixes

- Respect overrides in all direct-dependency iterators ([#2742](https://github.com/astral-sh/uv/pull/2742))
- Respect subdirectories when reading static metadata ([#2728](https://github.com/astral-sh/uv/pull/2728))

## 0.1.26

### Bug fixes

- Bump simple cache version ([#2712](https://github.com/astral-sh/uv/pull/2712))

## 0.1.25

### Breaking changes

- Limit overrides and constraints to `requirements.txt` format ([#2632](https://github.com/astral-sh/uv/pull/2632))

### Enhancements

- Accept `setup.py` and `setup.cfg` files in compile ([#2634](https://github.com/astral-sh/uv/pull/2634))
- Add `--no-binary` and `--only-binary` support
to `requirements.txt` ([#2680](https://github.com/astral-sh/uv/pull/2680))
- Allow pre-releases, locals, and URLs in non-editable path
requirements ([#2671](https://github.com/astral-sh/uv/pull/2671))
- Use PEP 517 to extract dynamic `pyproject.toml` metadata ([#2633](https://github.com/astral-sh/uv/pull/2633))
- Add `Editable project location` and `Required-by` to `pip show` ([#2589](https://github.com/astral-sh/uv/pull/2589))
- Avoid `prepare_metadata_for_build_wheel` calls for Hatch packages with dynamic
dependencies ([#2645](https://github.com/astral-sh/uv/pull/2645))
- Fall back to PEP 517 hooks for non-compliant PEP 621 metadata ([#2662](https://github.com/astral-sh/uv/pull/2662))
- Support `file://localhost/` schemes ([#2657](https://github.com/astral-sh/uv/pull/2657))
- Use normal resolver in `pip sync` ([#2696](https://github.com/astral-sh/uv/pull/2696))

### CLI

- Disallow `pyproject.toml` from `pip uninstall -r` ([#2663](https://github.com/astral-sh/uv/pull/2663))
- Unhide `--emit-index-url` and `--emit-find-links` ([#2691](https://github.com/astral-sh/uv/pull/2691))
- Use dense formatting for requirement version specifiers in
diagnostics ([#2601](https://github.com/astral-sh/uv/pull/2601))

### Performance

- Add an in-memory cache for Git references ([#2682](https://github.com/astral-sh/uv/pull/2682))
- Do not force-recompile `.pyc` files ([#2642](https://github.com/astral-sh/uv/pull/2642))
- Read package metadata from `pyproject.toml` when it is statically
defined ([#2676](https://github.com/astral-sh/uv/pull/2676))

### Bug fixes

- Don't error on multiple matching index URLs ([#2627](https://github.com/astral-sh/uv/pull/2627))
- Extract local versions from direct URL requirements ([#2624](https://github.com/astral-sh/uv/pull/2624))
- Respect `--no-index` with `--find-links` in `pip sync` ([#2692](https://github.com/astral-sh/uv/pull/2692))
- Use `Scripts` folder for virtualenv activation prompt ([#2690](https://github.com/astral-sh/uv/pull/2690))

## 0.1.24

### Breaking changes

- `uv pip uninstall` no longer supports specifying targets with the `-e` / `--editable`
flag ([#2577](https://github.com/astral-sh/uv/pull/2577))

### Enhancements

- Add a garbage collection mechanism to the CLI ([#1217](https://github.com/astral-sh/uv/pull/1217))
- Add progress reporting for named requirement resolution ([#2605](https://github.com/astral-sh/uv/pull/2605))
- Add support for parsing unnamed URL requirements ([#2567](https://github.com/astral-sh/uv/pull/2567))
- Add support for unnamed local directory requirements ([#2571](https://github.com/astral-sh/uv/pull/2571))
- Enable PEP 517 builds for unnamed requirements ([#2600](https://github.com/astral-sh/uv/pull/2600))
- Enable install audits without resolving named requirements ([#2575](https://github.com/astral-sh/uv/pull/2575))
- Enable unnamed requirements for direct URLs ([#2569](https://github.com/astral-sh/uv/pull/2569))
- Respect HTTP client options when reading remote requirements
files ([#2434](https://github.com/astral-sh/uv/pull/2434))
- Use PEP 517 build hooks to resolve unnamed requirements ([#2604](https://github.com/astral-sh/uv/pull/2604))
- Use c-string literals and update trampolines ([#2590](https://github.com/astral-sh/uv/pull/2590))
- Support unnamed requirements directly in `uv pip uninstall` ([#2577](https://github.com/astral-sh/uv/pull/2577))
- Add support for unnamed Git and HTTP requirements ([#2578](https://github.com/astral-sh/uv/pull/2578))
- Make self-update an opt-in Cargo feature ([#2606](https://github.com/astral-sh/uv/pull/2606))
- Update minimum rust version (cargo) to 1.76 ([#2618](https://github.com/astral-sh/uv/pull/2618))

### Bug fixes

- Fix self-updates on Windows ([#2598](https://github.com/astral-sh/uv/pull/2598))
- Fix authentication with usernames that contain `@` characters ([#2592](https://github.com/astral-sh/uv/pull/2592))
- Do not error when there are warnings on Python interpreter stderr ([#2599](https://github.com/astral-sh/uv/pull/2599))
- Prevent discovery of cache gitignore when building distributions ([#2615](https://github.com/astral-sh/uv/pull/2615))

### Rust API

- Make `InstallDist.direct_url` public ([#2584](https://github.com/astral-sh/uv/pull/2584))
- Make `AllowedYanks` public ([#2608](https://github.com/astral-sh/uv/pull/2608))

### Documentation

- Fix badge to current CI status ([#2612](https://github.com/astral-sh/uv/pull/2612))

## 0.1.23

### Enhancements

- Implement `--no-strip-extras` to preserve extras in compilation ([#2555](https://github.com/astral-sh/uv/pull/2555))
- Preserve hashes for pinned packages when compiling
without `--upgrade` ([#2532](https://github.com/astral-sh/uv/pull/2532))
- Add a `uv self update` command ([#2228](https://github.com/astral-sh/uv/pull/2228))
- Use relative paths for user-facing messages ([#2559](https://github.com/astral-sh/uv/pull/2559))
- Add `CUSTOM_COMPILE_COMMAND` support to `uv pip compile` ([#2554](https://github.com/astral-sh/uv/pull/2554))
- Add SHA384 and SHA512 hash algorithms ([#2534](https://github.com/astral-sh/uv/pull/2534))
- Treat uninstallable packages as warnings, rather than errors ([#2557](https://github.com/astral-sh/uv/pull/2557))

### Bug fixes

- Allow `VIRTUAL_ENV` to take precedence over `CONDA_PREFIX` ([#2574](https://github.com/astral-sh/uv/pull/2574))
- Ensure mtime of site packages is updated during wheel
installation ([#2545](https://github.com/astral-sh/uv/pull/2545))
- Re-test validity after every lenient parsing change ([#2550](https://github.com/astral-sh/uv/pull/2550))
- Run interpreter discovery under `-I` mode ([#2552](https://github.com/astral-sh/uv/pull/2552))
- Search in both `purelib` and `platlib` for site-packages
population ([#2537](https://github.com/astral-sh/uv/pull/2537))
- Fix wheel builds and uploads for musl ARM ([#2518](https://github.com/astral-sh/uv/pull/2518))

### Documentation

- Add `--link-mode` defaults to CLI ([#2549](https://github.com/astral-sh/uv/pull/2549))
- Add an example workflow for compiling the current environment's
packages ([#1968](https://github.com/astral-sh/uv/pull/1968))
- Add `uv pip check diagnostics` to `PIP_COMPATIBILITY.md` ([#2544](https://github.com/astral-sh/uv/pull/2544))

## 0.1.22

### Enhancements

- Add support for PyTorch-style local version semantics ([#2430](https://github.com/astral-sh/uv/pull/2430))
- Add support for Hatch's `{root:uri}` paths in editable installs ([#2492](https://github.com/astral-sh/uv/pull/2492))
- Implement `uv pip check` ([#2397](https://github.com/astral-sh/uv/pull/2397))
- Add pip-like linehaul information to user agent ([#2493](https://github.com/astral-sh/uv/pull/2493))
- Add additional ARM targets to release ([#2417](https://github.com/astral-sh/uv/pull/2417))

### Bug fixes

- Allow direct file path requirements to include fragments ([#2502](https://github.com/astral-sh/uv/pull/2502))
- Avoid panicking on cannot-be-a-base URLs ([#2461](https://github.com/astral-sh/uv/pull/2461))
- Drop `macosx_10_0` from compatible wheel tags on `aarch64` ([#2496](https://github.com/astral-sh/uv/pull/2496))
- Fix operating system detection on \*BSD ([#2505](https://github.com/astral-sh/uv/pull/2505))
- Fix priority of ABI tags ([#2489](https://github.com/astral-sh/uv/pull/2489))
- Fix priority of platform tags for manylinux ([#2483](https://github.com/astral-sh/uv/pull/2483))
- Make > operator exclude post and local releases ([#2471](https://github.com/astral-sh/uv/pull/2471))
- Re-add support for pyenv shims ([#2503](https://github.com/astral-sh/uv/pull/2503))
- Validate required package names against wheel package names ([#2516](https://github.com/astral-sh/uv/pull/2516))

## 0.1.21

### Enhancements

- Loosen `.dist-info` validation to accept arbitrary versions ([#2441](https://github.com/astral-sh/uv/pull/2441))

### Bug fixes

- Fix macOS architecture detection on i386 machines ([#2454](https://github.com/astral-sh/uv/pull/2454))

## 0.1.20

### Bug fixes

- Add in-URL credentials to store prior to creating requests ([#2446](https://github.com/astral-sh/uv/pull/2446))
- Error when direct URL requirements don't match `Requires-Python` ([#2196](https://github.com/astral-sh/uv/pull/2196))

## 0.1.19

### Configuration

- Add `UV_NATIVE_TLS` environment variable ([#2412](https://github.com/astral-sh/uv/pull/2412))
- Allow `SSL_CERT_FILE` without requiring `--native-tls` ([#2401](https://github.com/astral-sh/uv/pull/2401))
- Add support for retrieving credentials from `keyring` ([#2254](https://github.com/astral-sh/uv/pull/2254))

### Bug fixes

- Add backoff for transient Windows failures ([#2419](https://github.com/astral-sh/uv/pull/2419))
- Move architecture and operating system probing to Python ([#2381](https://github.com/astral-sh/uv/pull/2381))
- Respect `--native-tls` in `venv` ([#2433](https://github.com/astral-sh/uv/pull/2433))
- Treat non-existent site-packages as empty ([#2413](https://github.com/astral-sh/uv/pull/2413))

### Documentation

- Document HTTP authentication ([#2425](https://github.com/astral-sh/uv/pull/2425))

### Performance

- Improve performance of version range operations ([#2421](https://github.com/astral-sh/uv/pull/2421))

## 0.1.18

### Breaking changes

Users that rely on native root certificates (or the `SSL_CERT_FILE`) environment variable must now
pass the `--native-tls` command-line flag to enable this behavior.

- Enable TLS native root toggling at runtime ([#2362](https://github.com/astral-sh/uv/pull/2362))

### Enhancements

- Add `--dry-run` flag to `uv pip install` ([#1436](https://github.com/astral-sh/uv/pull/1436))
- Implement "Requires" field in `pip show` ([#2347](https://github.com/astral-sh/uv/pull/2347))
- Remove `wheel` from default PEP 517 backend ([#2341](https://github.com/astral-sh/uv/pull/2341))
- Add `UV_SYSTEM_PYTHON` environment variable as alias
to `--system` ([#2354](https://github.com/astral-sh/uv/pull/2354))
- Add a `-vv` log level and make `-v` more readable ([#2301](https://github.com/astral-sh/uv/pull/2301))

### Bug fixes

- Expand environment variables prior to detecting scheme ([#2394](https://github.com/astral-sh/uv/pull/2394))
- Fix bug where `--no-binary :all:` prevented build of editable
packages ([#2393](https://github.com/astral-sh/uv/pull/2393))
- Ignore inverse dependencies when building graph ([#2360](https://github.com/astral-sh/uv/pull/2360))
- Skip prefetching when `--no-deps` is specified ([#2373](https://github.com/astral-sh/uv/pull/2373))
- Trim injected `python_version` marker to (major, minor) ([#2395](https://github.com/astral-sh/uv/pull/2395))
- Wait for request stream to flush before returning resolution ([#2374](https://github.com/astral-sh/uv/pull/2374))
- Write relative paths for scripts in data directory ([#2348](https://github.com/astral-sh/uv/pull/2348))
- Add dedicated error message for direct filesystem paths in
requirements ([#2369](https://github.com/astral-sh/uv/pull/2369))

## 0.1.17

### Enhancements

- Allow more-precise Git URLs to override less-precise Git URLs ([#2285](https://github.com/astral-sh/uv/pull/2285))
- Add support for Metadata 2.2 ([#2293](https://github.com/astral-sh/uv/pull/2293))
- Added ability to select bytecode invalidation mode of generated `.pyc`
files ([#2297](https://github.com/astral-sh/uv/pull/2297))
- Add `Seek` fallback for zip files with data descriptors ([#2320](https://github.com/astral-sh/uv/pull/2320))

### Bug fixes

- Support reading UTF-16 requirements files ([#2283](https://github.com/astral-sh/uv/pull/2283))
- Trim rows in `pip list` ([#2298](https://github.com/astral-sh/uv/pull/2298))
- Avoid using setuptools shim of distutils ([#2305](https://github.com/astral-sh/uv/pull/2305))
- Communicate PEP 517 hook results via files ([#2314](https://github.com/astral-sh/uv/pull/2314))
- Increase default buffer size for wheel and source downloads ([#2319](https://github.com/astral-sh/uv/pull/2319))
- Add `Accept-Encoding: identity` to remaining stream paths ([#2321](https://github.com/astral-sh/uv/pull/2321))
- Avoid duplicating authorization header with netrc ([#2325](https://github.com/astral-sh/uv/pull/2325))
- Remove duplicate `INSTALLER` in `RECORD` ([#2336](https://github.com/astral-sh/uv/pull/2336))

### Documentation

- Add a custom suggestion to install wheel into the build
environment ([#2307](https://github.com/astral-sh/uv/pull/2307))
- Document the environment variables that uv respects ([#2318](https://github.com/astral-sh/uv/pull/2318))

## 0.1.16

### Enhancements

- Add support for `--no-build-isolation` ([#2258](https://github.com/astral-sh/uv/pull/2258))
- Add support for `--break-system-packages` ([#2249](https://github.com/astral-sh/uv/pull/2249))
- Add support for `.netrc` authentication ([#2241](https://github.com/astral-sh/uv/pull/2241))
- Add support for `--format=freeze` and `--format=json`
in `uv pip list` ([#1998](https://github.com/astral-sh/uv/pull/1998))
- Add support for remote `https://` requirements files (#1332) ([#2081](https://github.com/astral-sh/uv/pull/2081))
- Implement `uv pip show` ([#2115](https://github.com/astral-sh/uv/pull/2115))
- Allow `UV_PRERELEASE` to be set via environment variable ([#2240](https://github.com/astral-sh/uv/pull/2240))
- Include exit code for build failures ([#2108](https://github.com/astral-sh/uv/pull/2108))
- Query interpreter to determine correct `virtualenv` paths, enabling `uv venv` with PyPy and
others ([#2188](https://github.com/astral-sh/uv/pull/2188))
- Respect non-`sysconfig`-based system Pythons, enabling `--system` installs on Debian and
others ([#2193](https://github.com/astral-sh/uv/pull/2193))

### Bug fixes

- Fallback to fresh request on non-validating 304 ([#2218](https://github.com/astral-sh/uv/pull/2218))
- Add `.stdout()` and `.stderr()` outputs to `Printer` ([#2227](https://github.com/astral-sh/uv/pull/2227))
- Close `RECORD` after reading entries during uninstall ([#2259](https://github.com/astral-sh/uv/pull/2259))
- Fix Conda Python detection on Windows ([#2279](https://github.com/astral-sh/uv/pull/2279))
- Fix parsing requirement where a variable follows an operator without a
space ([#2273](https://github.com/astral-sh/uv/pull/2273))
- Prefer more recent minor versions in wheel tags ([#2263](https://github.com/astral-sh/uv/pull/2263))
- Retry on Python interpreter launch failures during `--compile` ([#2278](https://github.com/astral-sh/uv/pull/2278))
- Show appropriate activation command based on shell detection ([#2221](https://github.com/astral-sh/uv/pull/2221))
- Escape Windows paths with spaces in `venv` activation command ([#2223](https://github.com/astral-sh/uv/pull/2223))
- Add specialized activation message for `cmd.exe` ([#2226](https://github.com/astral-sh/uv/pull/2226))
- Cache wheel metadata in no-PEP 658 fallback ([#2255](https://github.com/astral-sh/uv/pull/2255))
- Use reparse points to detect Windows installer shims ([#2284](https://github.com/astral-sh/uv/pull/2284))

### Documentation

- Add `PIP_COMPATIBILITY.md` to document known deviations
from `pip` ([#2244](https://github.com/astral-sh/uv/pull/2244))

## 0.1.15

### Enhancements

- Add a `--compile` option to `install` to enable bytecode
compilation ([#2086](https://github.com/astral-sh/uv/pull/2086))
- Expose the `--exclude-newer` flag to limit candidate packages based on
date ([#2166](https://github.com/astral-sh/uv/pull/2166))
- Add `uv` version to user agent ([#2136](https://github.com/astral-sh/uv/pull/2136))

### Bug fixes

- Set `.metadata` suffix on URL path ([#2123](https://github.com/astral-sh/uv/pull/2123))
- Fallback to non-range requests when HEAD returns 404 ([#2186](https://github.com/astral-sh/uv/pull/2186))
- Allow direct URLs in optional dependencies in editables ([#2206](https://github.com/astral-sh/uv/pull/2206))
- Allow empty values in WHEEL files ([#2170](https://github.com/astral-sh/uv/pull/2170))
- Avoid Windows Store shims in `--python python3`-like invocations ([#2212](https://github.com/astral-sh/uv/pull/2212))
- Expand Windows shim detection to include `python3.12.exe` ([#2209](https://github.com/astral-sh/uv/pull/2209))
- HTML-decode URLs in HTML indexes ([#2215](https://github.com/astral-sh/uv/pull/2215))
- Make direct dependency detection respect markers ([#2207](https://github.com/astral-sh/uv/pull/2207))
- Respect `py --list-paths` fallback in `--python python3` invocations on
Windows ([#2214](https://github.com/astral-sh/uv/pull/2214))
- Respect local freshness when auditing installed environment ([#2169](https://github.com/astral-sh/uv/pull/2169))
- Respect markers on URL dependencies in editables ([#2176](https://github.com/astral-sh/uv/pull/2176))
- Respect nested editable requirements in parser ([#2204](https://github.com/astral-sh/uv/pull/2204))
- Run Windows against Python 3.13 ([#2171](https://github.com/astral-sh/uv/pull/2171))
- Error when editables don't match `Requires-Python` ([#2194](https://github.com/astral-sh/uv/pull/2194))

## 0.1.14

### Enhancements

- Add support for `--system-site-packages` in `uv venv` ([#2101](https://github.com/astral-sh/uv/pull/2101))
- Add support for Python installed from Windows Store ([#2122](https://github.com/astral-sh/uv/pull/2122))
- Expand environment variables in `-r` and `-c` subfile paths ([#2143](https://github.com/astral-sh/uv/pull/2143))
- Treat empty index URL strings as null instead of erroring ([#2137](https://github.com/astral-sh/uv/pull/2137))
- Use space as delimiter for `UV_EXTRA_INDEX_URL` ([#2140](https://github.com/astral-sh/uv/pull/2140))
- Report line and column numbers in `requirements.txt` parser
errors ([#2100](https://github.com/astral-sh/uv/pull/2100))
- Improve error messages when `uv` is offline ([#2110](https://github.com/astral-sh/uv/pull/2110))

### Bug fixes

- Future-proof the `pip` entrypoints special-case ([#1982](https://github.com/astral-sh/uv/pull/1982))
- Allow empty extras in `pep508-rs` and add more corner case to
tests ([#2128](https://github.com/astral-sh/uv/pull/2128))
- Adjust base Python lookup logic for Windows to respect Windows
Store ([#2121](https://github.com/astral-sh/uv/pull/2121))
- Consider editable dependencies to be 'direct' for `--resolution` ([#2114](https://github.com/astral-sh/uv/pull/2114))
- Preserve environment variables in resolved Git dependencies ([#2125](https://github.com/astral-sh/uv/pull/2125))
- Use `prefix` instead of `base_prefix` for environment root ([#2117](https://github.com/astral-sh/uv/pull/2117))
- Wrap unsafe script shebangs in `/bin/sh` ([#2097](https://github.com/astral-sh/uv/pull/2097))
- Make WHEEL parsing error line numbers one indexed ([#2151](https://github.com/astral-sh/uv/pull/2151))
- Determine `site-packages` path based on implementation name ([#2094](https://github.com/astral-sh/uv/pull/2094))

### Documentation

- Add caveats on `--system` support to the README ([#2131](https://github.com/astral-sh/uv/pull/2131))
- Add instructions for `SSL_CERT_FILE` env var ([#2124](https://github.com/astral-sh/uv/pull/2124))

## 0.1.13

### Bug fixes

- Prioritize `PATH` over `py --list-paths` in Windows selection ([#2057](https://github.com/astral-sh/uv/pull/2057)).
This fixes an issue in which the `--system` flag would not work correctly on Windows in GitHub Actions.
- Avoid canonicalizing user-provided interpreters ([#2072](https://github.com/astral-sh/uv/pull/2072)). This fixes an
issue in which the `--python` flag would not work correctly with pyenv and other interpreters.
- Allow pre-releases for requirements in constraints files ([#2069](https://github.com/astral-sh/uv/pull/2069))
- Avoid truncating EXTERNALLY-MANAGED error message ([#2073](https://github.com/astral-sh/uv/pull/2073))
- Extend activation highlighting to entire `venv` command ([#2070](https://github.com/astral-sh/uv/pull/2070))
- Reverse the order of `--index-url` and `--extra-index-url`
priority ([#2083](https://github.com/astral-sh/uv/pull/2083))
- Avoid assuming `RECORD` file is in `platlib` ([#2091](https://github.com/astral-sh/uv/pull/2091))

## 0.1.12

### CLI

- Add a `--python` flag to allow installation into arbitrary Python
interpreters ([#2000](https://github.com/astral-sh/uv/pull/2000))
- Add a `--system` flag for opt-in non-virtualenv installs ([#2046](https://github.com/astral-sh/uv/pull/2046))

### Enhancements

- Add a `--pre` alias for `--prerelease=allow` ([#2049](https://github.com/astral-sh/uv/pull/2049))
- Enable `freeze` and `list` to introspect non-virtualenv Pythons ([#2033](https://github.com/astral-sh/uv/pull/2033))
- Support environment variables in index URLs in requirements files ([#2036](https://github.com/astral-sh/uv/pull/2036))
- Add `--exclude-editable` and `--exclude` args to `uv pip list` ([#1985](https://github.com/astral-sh/uv/pull/1985))
- Always remove color codes from output file ([#2018](https://github.com/astral-sh/uv/pull/2018))
- Support recursive extras in direct `pyproject.toml` files ([#1990](https://github.com/astral-sh/uv/pull/1990))
- Un-cache editable requirements with dynamic metadata ([#2029](https://github.com/astral-sh/uv/pull/2029))
- Use a non-local lockfile for locking system interpreters ([#2045](https://github.com/astral-sh/uv/pull/2045))
- Surface the `EXTERNALLY-MANAGED` message to users ([#2032](https://github.com/astral-sh/uv/pull/2032))

## 0.1.11

### Enhancements

- Add support for pip-compile's `--unsafe-package` flag ([#1889](https://github.com/astral-sh/uv/pull/1889))
- Improve interpreter discovery logging ([#1909](https://github.com/astral-sh/uv/pull/1909))
- Implement `uv pip list` ([#1662](https://github.com/astral-sh/uv/pull/1662))
- Allow round-trip via `freeze` command ([#1936](https://github.com/astral-sh/uv/pull/1936))
- Don't write pip compile output to stdout with `-q` ([#1962](https://github.com/astral-sh/uv/pull/1962))
- Add long-form version output ([#1930](https://github.com/astral-sh/uv/pull/1930))

### Compatibility

- Accept single string for `backend-path` ([#1969](https://github.com/astral-sh/uv/pull/1969))
- Add compatibility for deprecated `python_implementation` marker ([#1933](https://github.com/astral-sh/uv/pull/1933))
- Generate versioned `pip` launchers ([#1918](https://github.com/astral-sh/uv/pull/1918))

### Bug fixes

- Avoid erroring for source distributions with symlinks in archive ([#1944](https://github.com/astral-sh/uv/pull/1944))
- Expand scope of archive timestamping ([#1960](https://github.com/astral-sh/uv/pull/1960))
- Gracefully handle virtual environments with conflicting packages ([#1893](https://github.com/astral-sh/uv/pull/1893))
- Invalidate dependencies when editables are updated ([#1955](https://github.com/astral-sh/uv/pull/1955))
- Make < exclusive for non-pre-release markers ([#1878](https://github.com/astral-sh/uv/pull/1878))
- Properly apply constraints in venv audit ([#1956](https://github.com/astral-sh/uv/pull/1956))
- Re-sync editables on-change ([#1959](https://github.com/astral-sh/uv/pull/1959))
- Remove current directory from PATH in PEP 517 hooks ([#1975](https://github.com/astral-sh/uv/pull/1975))
- Remove `--upgrade` and `--quiet` flags from generated output
files ([#1873](https://github.com/astral-sh/uv/pull/1873))
- Use full python version in `pyvenv.cfg` ([#1979](https://github.com/astral-sh/uv/pull/1979))

### Performance

- fix `uv pip install` handling of gzip'd response and PEP 691 ([#1978](https://github.com/astral-sh/uv/pull/1978))
- Remove `spawn_blocking` from version map ([#1966](https://github.com/astral-sh/uv/pull/1966))

### Documentation

- Clarify `lowest` vs. `lowest-direct` resolution strategies ([#1954](https://github.com/astral-sh/uv/pull/1954))
- Improve error message for network timeouts ([#1961](https://github.com/astral-sh/uv/pull/1961))

## 0.1.10

### Enhancements

- Omit `--find-links` from annotation header unless requested ([#1898](https://github.com/astral-sh/uv/pull/1898))
- Write to stdout when `--output-file` is present ([#1892](https://github.com/astral-sh/uv/pull/1892))

### Bug fixes

- Retain authentication when making range requests ([#1902](https://github.com/astral-sh/uv/pull/1902))
- Fix uv-created venv detection ([#1908](https://github.com/astral-sh/uv/pull/1908))
- Fix Windows `py` failure from spurious stderr ([#1885](https://github.com/astral-sh/uv/pull/1885))
- Ignore Python 2 installations when querying for interpreters ([#1905](https://github.com/astral-sh/uv/pull/1905))

## 0.1.9

### Enhancements

- Add support for `config_settings` in PEP 517 hooks ([#1833](https://github.com/astral-sh/uv/pull/1833))
- feat: allow passing extra config k,v pairs for pyvenv.cfg when creating a
venv ([#1852](https://github.com/astral-sh/uv/pull/1852))

### Bug fixes

- Ensure authentication is passed from the index url to distribution
files ([#1886](https://github.com/astral-sh/uv/pull/1886))
- Use `rustls-tls-native-roots` in `uv` crate ([#1888](https://github.com/astral-sh/uv/pull/1888))
- pep440: fix version ordering ([#1883](https://github.com/astral-sh/uv/pull/1883))
- Hide index URLs from header if not emitted ([#1835](https://github.com/astral-sh/uv/pull/1835))

### Documentation

- Add changelog ([#1881](https://github.com/astral-sh/uv/pull/1881))

## 0.1.8

### Bug fixes

- Allow duplicate URLs that resolve to the same canonical URL ([#1877](https://github.com/astral-sh/uv/pull/1877))
- Retain authentication attached to URLs when making requests to the same
host ([#1874](https://github.com/astral-sh/uv/pull/1874))
- Win Trampoline: Use Python executable path encoded in binary ([#1803](https://github.com/astral-sh/uv/pull/1803))
- Expose types to implement custom `ResolverProvider` ([#1862](https://github.com/astral-sh/uv/pull/1862))
- Search `PATH` when `python` can't be found with `py` ([#1711](https://github.com/astral-sh/uv/pull/1711))
- Avoid displaying "root" package when formatting terms ([#1871](https://github.com/astral-sh/uv/pull/1871))

### Documentation

- Use more universal windows install instructions ([#1811](https://github.com/astral-sh/uv/pull/1811))

### Rust API

- Expose types to implement custom ResolverProvider ([#1862](https://github.com/astral-sh/uv/pull/1862))

## 0.1.7

### Enhancements

- Stream zip archive when fetching non-range-request metadata ([#1792](https://github.com/astral-sh/uv/pull/1792))
- Support setting request timeout with `UV_HTTP_TIMEOUT`
and `HTTP_TIMEOUT` ([#1780](https://github.com/astral-sh/uv/pull/1780))
- Improve error message when git ref cannot be fetched ([#1826](https://github.com/astral-sh/uv/pull/1826))

### Configuration

- Implement `--annotation-style` parameter for `uv pip compile` ([#1679](https://github.com/astral-sh/uv/pull/1679))

### Bug fixes

- Add fixup for `prefect<1.0.0` ([#1825](https://github.com/astral-sh/uv/pull/1825))
- Add support for `>dev` specifier ([#1776](https://github.com/astral-sh/uv/pull/1776))
- Avoid enforcing URL correctness for installed distributions ([#1793](https://github.com/astral-sh/uv/pull/1793))
- Don't expect pinned packages for editables with non-existent
extras ([#1847](https://github.com/astral-sh/uv/pull/1847))
- Linker copies files as a fallback when ref-linking fails ([#1773](https://github.com/astral-sh/uv/pull/1773))
- Move conflicting dependencies into PubGrub ([#1796](https://github.com/astral-sh/uv/pull/1796))
- Normalize `VIRTUAL_ENV` path in activation scripts ([#1817](https://github.com/astral-sh/uv/pull/1817))
- Preserve executable bit when untarring archives ([#1790](https://github.com/astral-sh/uv/pull/1790))
- Retain passwords in Git URLs ([#1717](https://github.com/astral-sh/uv/pull/1717))
- Sort output when installing seed packages ([#1822](https://github.com/astral-sh/uv/pull/1822))
- Treat ARM wheels as higher-priority than universal ([#1843](https://github.com/astral-sh/uv/pull/1843))
- Use `git` command to fetch repositories instead of `libgit2` for robust SSH
support ([#1781](https://github.com/astral-sh/uv/pull/1781))
- Use redirected URL as base for relative paths ([#1816](https://github.com/astral-sh/uv/pull/1816))
- Use the right marker for the `implementation` field
of `pyvenv.cfg` ([#1785](https://github.com/astral-sh/uv/pull/1785))
- Wait for distribution metadata with `--no-deps` ([#1812](https://github.com/astral-sh/uv/pull/1812))
- platform-host: check /bin/sh, then /bin/dash and then /bin/ls ([#1818](https://github.com/astral-sh/uv/pull/1818))
- Ensure that builds within the cache aren't considered Git
repositories ([#1782](https://github.com/astral-sh/uv/pull/1782))
- Strip trailing `+` from version number of local Python builds ([#1771](https://github.com/astral-sh/uv/pull/1771))

### Documentation

- Add docs for git authentication ([#1844](https://github.com/astral-sh/uv/pull/1844))
- Update venv activation for windows ([#1836](https://github.com/astral-sh/uv/pull/1836))
- Update README.md to include extras example ([#1806](https://github.com/astral-sh/uv/pull/1806))

## 0.1.6

### Enhancements

- Expose find_uv_bin and declare typing support ([#1728](https://github.com/astral-sh/uv/pull/1728))
- Implement `uv cache dir` ([#1734](https://github.com/astral-sh/uv/pull/1734))
- Support `venv --prompt` ([#1570](https://github.com/astral-sh/uv/pull/1570))
- Print activation instructions for a venv after one has been
created ([#1580](https://github.com/astral-sh/uv/pull/1580))

### CLI

- Add shell completions generation ([#1675](https://github.com/astral-sh/uv/pull/1675))
- Move `uv clean` to `uv cache clean` ([#1733](https://github.com/astral-sh/uv/pull/1733))
- Allow `-f` alias for `--find-links` ([#1735](https://github.com/astral-sh/uv/pull/1735))

### Configuration

- Control pip timeout duration via environment variable ([#1694](https://github.com/astral-sh/uv/pull/1694))

### Bug fixes

- Add support for absolute paths on Windows ([#1725](https://github.com/astral-sh/uv/pull/1725))
- Don't preserve timestamp in streaming unzip ([#1749](https://github.com/astral-sh/uv/pull/1749))
- Ensure extras trigger an install ([#1727](https://github.com/astral-sh/uv/pull/1727))
- Only preserve the executable bit ([#1743](https://github.com/astral-sh/uv/pull/1743))
- Preserve trailing slash for `--find-links` URLs ([#1720](https://github.com/astral-sh/uv/pull/1720))
- Respect `--index-url` provided via requirements.txt ([#1719](https://github.com/astral-sh/uv/pull/1719))
- Set index URLs for seeding venv ([#1755](https://github.com/astral-sh/uv/pull/1755))
- Support dotted function paths for script entrypoints ([#1622](https://github.com/astral-sh/uv/pull/1622))
- Support recursive extras for URL dependencies ([#1729](https://github.com/astral-sh/uv/pull/1729))
- Better error message for missing space before semicolon in
requirements ([#1746](https://github.com/astral-sh/uv/pull/1746))
- Add warning when dependencies are empty with Poetry metadata ([#1650](https://github.com/astral-sh/uv/pull/1650))
- Ignore invalid extras from PyPI ([#1731](https://github.com/astral-sh/uv/pull/1731))
- Improve Poetry warning ([#1730](https://github.com/astral-sh/uv/pull/1730))
- Remove uv version from uv pip compile header ([#1716](https://github.com/astral-sh/uv/pull/1716))
- Fix handling of range requests on servers that return "Method not
allowed" ([#1713](https://github.com/astral-sh/uv/pull/1713))
- re-introduce cache healing when we see an invalid cache entry ([#1707](https://github.com/astral-sh/uv/pull/1707))

### Documentation

- Clarify Windows install command in README.md ([#1751](https://github.com/astral-sh/uv/pull/1751))
- Add instructions for installing on Arch Linux ([#1765](https://github.com/astral-sh/uv/pull/1765))

### Rust API

- Allow passing in a custom reqwest Client ([#1745](https://github.com/astral-sh/uv/pull/1745))

## 0.1.5

### Enhancements

- Add `CACHEDIR.TAG` to uv-created virtualenvs ([#1653](https://github.com/astral-sh/uv/pull/1653))

### Bug fixes

- Build source distributions in the cache directory instead of the global temporary
directory ([#1628](https://github.com/astral-sh/uv/pull/1628))
- Do not remove uv itself on pip sync ([#1649](https://github.com/astral-sh/uv/pull/1649))
- Ensure we retain existing environment variables
during `python -m uv` ([#1667](https://github.com/astral-sh/uv/pull/1667))
- Add yank warnings at end of messages ([#1669](https://github.com/astral-sh/uv/pull/1669))

### Documentation

- Add brew to readme ([#1629](https://github.com/astral-sh/uv/pull/1629))
- Document RUST_LOG=trace for additional logging verbosity ([#1670](https://github.com/astral-sh/uv/pull/1670))
- Document local testing instructions ([#1672](https://github.com/astral-sh/uv/pull/1672))
- Minimal markdown nits ([#1664](https://github.com/astral-sh/uv/pull/1664))
- Use `--override` rather than `-o` to specify overrides in
README.md ([#1668](https://github.com/astral-sh/uv/pull/1668))
- Remove setuptools & wheel from seed packages on Python 3.12+ (
#1602) ([#1613](https://github.com/astral-sh/uv/pull/1613))

## 0.1.4

### Enhancements

- Add CMD support ([#1523](https://github.com/astral-sh/uv/pull/1523))
- Improve tracing when encountering invalid `requires-python`
values ([#1568](https://github.com/astral-sh/uv/pull/1568))

### Bug fixes

- Add graceful fallback for Artifactory indexes ([#1574](https://github.com/astral-sh/uv/pull/1574))
- Allow URL requirements in editable installs ([#1614](https://github.com/astral-sh/uv/pull/1614))
- Allow repeated dependencies when installing ([#1558](https://github.com/astral-sh/uv/pull/1558))
- Always run `get_requires_for_build_wheel` ([#1590](https://github.com/astral-sh/uv/pull/1590))
- Avoid propagating top-level options to sub-resolutions ([#1607](https://github.com/astral-sh/uv/pull/1607))
- Consistent use of `BIN_NAME` in activation scripts ([#1577](https://github.com/astral-sh/uv/pull/1577))
- Enforce URL constraints for non-URL dependencies ([#1565](https://github.com/astral-sh/uv/pull/1565))
- Allow non-nested archives for `hexdump` and others ([#1564](https://github.com/astral-sh/uv/pull/1564))
- Avoid using `white` coloring in terminal output ([#1576](https://github.com/astral-sh/uv/pull/1576))
- Bump simple metadata cache version ([#1617](https://github.com/astral-sh/uv/pull/1617))
- Better error messages on expect failures in resolver ([#1583](https://github.com/astral-sh/uv/pull/1583))

### Documentation

- Add license to activator scripts ([#1610](https://github.com/astral-sh/uv/pull/1610))

## 0.1.3

### Enhancements

- Add support for `UV_EXTRA_INDEX_URL` ([#1515](https://github.com/astral-sh/uv/pull/1515))
- Use the system trust store for HTTPS requests ([#1512](https://github.com/astral-sh/uv/pull/1512))
- Automatically detect virtual environments when used
via `python -m uv` ([#1504](https://github.com/astral-sh/uv/pull/1504))
- Add warning for empty requirements files ([#1519](https://github.com/astral-sh/uv/pull/1519))
- Support MD5 hashes ([#1556](https://github.com/astral-sh/uv/pull/1556))

### Bug fixes

- Add support for extras in editable requirements ([#1531](https://github.com/astral-sh/uv/pull/1531))
- Apply percent-decoding to file-based URLs ([#1541](https://github.com/astral-sh/uv/pull/1541))
- Apply percent-decoding to filepaths in HTML find-links ([#1544](https://github.com/astral-sh/uv/pull/1544))
- Avoid attempting rename in copy fallback path ([#1546](https://github.com/astral-sh/uv/pull/1546))
- Fix list rendering in `venv --help` output ([#1459](https://github.com/astral-sh/uv/pull/1459))
- Fix trailing commas on `Requires-Python` in HTML indexes ([#1507](https://github.com/astral-sh/uv/pull/1507))
- Read from `/bin/sh` if `/bin/ls` cannot be found when determining libc
path ([#1433](https://github.com/astral-sh/uv/pull/1433))
- Remove URL encoding when determining file name ([#1555](https://github.com/astral-sh/uv/pull/1555))
- Support recursive extras ([#1435](https://github.com/astral-sh/uv/pull/1435))
- Use comparable representation for `PackageId` ([#1543](https://github.com/astral-sh/uv/pull/1543))
- fix OS detection for Alpine Linux ([#1545](https://github.com/astral-sh/uv/pull/1545))
- only parse /bin/sh (not /bin/ls) ([#1493](https://github.com/astral-sh/uv/pull/1493))
- pypi-types: fix lenient requirement parsing ([#1529](https://github.com/astral-sh/uv/pull/1529))
- Loosen package script regexp to match spec ([#1482](https://github.com/astral-sh/uv/pull/1482))
- Use string display instead of debug for url parse trace ([#1498](https://github.com/astral-sh/uv/pull/1498))

### Documentation

- Provide example of file based package install. ([#1424](https://github.com/astral-sh/uv/pull/1424))
- Adjust link ([#1434](https://github.com/astral-sh/uv/pull/1434))
- Add troubleshooting section to benchmarks guide ([#1485](https://github.com/astral-sh/uv/pull/1485))
- infra: source github templates ([#1425](https://github.com/astral-sh/uv/pull/1425))

## 0.1.2

### Enhancements

- Add `--upgrade` support to `pip install` ([#1379](https://github.com/astral-sh/uv/pull/1379))
- Add `-U`/`-P` short flags for `--upgrade`/`--upgrade-package` ([#1394](https://github.com/astral-sh/uv/pull/1394))
- Add `UV_NO_CACHE` environment variable ([#1383](https://github.com/astral-sh/uv/pull/1383))
- uv-cache: Add hidden alias for --no-cache-dir ([#1380](https://github.com/astral-sh/uv/pull/1380))

### Bug fixes

- Add fix-up for invalid star comparison with major-only version ([#1410](https://github.com/astral-sh/uv/pull/1410))
- Add fix-up for trailing comma with trailing space ([#1409](https://github.com/astral-sh/uv/pull/1409))
- Allow empty fragments in HTML parser ([#1443](https://github.com/astral-sh/uv/pull/1443))
- Fix search for `python.exe` on Windows ([#1381](https://github.com/astral-sh/uv/pull/1381))
- Ignore invalid extra named `.none` ([#1428](https://github.com/astral-sh/uv/pull/1428))
- Parse `-r` and `-c` entries as relative to containing file ([#1421](https://github.com/astral-sh/uv/pull/1421))
- Avoid import contextlib in `_virtualenv` ([#1406](https://github.com/astral-sh/uv/pull/1406))
- Decode HTML escapes when extracting SHA ([#1440](https://github.com/astral-sh/uv/pull/1440))
- Fix broken URLs parsed from relative paths in registries ([#1413](https://github.com/astral-sh/uv/pull/1413))
- Improve error message for invalid sdist archives ([#1389](https://github.com/astral-sh/uv/pull/1389))

### Documentation

- Re-add license badge to the README ([#1333](https://github.com/astral-sh/uv/pull/1333))
- Replace "novel" in README ([#1365](https://github.com/astral-sh/uv/pull/1365))
- Tweak some grammar in the README ([#1387](https://github.com/astral-sh/uv/pull/1387))
- Update README.md to include venv activate ([#1411](https://github.com/astral-sh/uv/pull/1411))
- Update wording and add `alt` tag ([#1423](https://github.com/astral-sh/uv/pull/1423))

## 0.1.1

### Bug fixes

- Fix bug where `python3` is not found in the global path ([#1351](https://github.com/astral-sh/uv/pull/1351))

### Documentation

- Fix diagram alignment ([#1354](https://github.com/astral-sh/uv/pull/1354))
- Grammar nit ([#1345](https://github.com/astral-sh/uv/pull/1345))

<!-- prettier-ignore-end -->



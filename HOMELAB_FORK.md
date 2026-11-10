# zollak fork of keesschollaart81/vscode-home-assistant

- `dev` = untouched mirror of upstream `dev` (upstream's default branch). `master` upstream = release branch (v2.2.0).
- `homelab` = upstream `dev` + upstream PR #4072 (include_dir_* / !env_var diagnostic filter, template plural keys,
  MQTT default_entity_id, for_each lists, MQTT device identifiers). Not built or deployed.

## Status (2026-11-10)
Measured on the HA config (31 yaml files) with a local harness: #4072 removes only the include-tag false positives
(5 of ~1090 diagnostics). The bulk comes from the schema not knowing legacy `platform: rest` sensor/switch items.
Decision (Zoltán, TG 5012): no deployment and no upstream PR for the rest schema now; the fork stays for later.
Details: homelab-config `servers/ha/changelog/20261110_vscode_ha_extension_false_warnings.md`.

## Differences vs upstream
| Change | Source | State |
|---|---|---|
| PR #4072 merged | upstream PR (Brownys), open upstream | carried; drop when upstream merges it |

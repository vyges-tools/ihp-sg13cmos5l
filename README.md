> [!IMPORTANT]
> **SUPERSEDED 2026-09-01 — use [`vyges-tools/ihp-open-pdk`](https://github.com/vyges-tools/ihp-open-pdk) on its `dev` branch.**
>
> Upstream merged this overlay into IHP-Open-PDK (PR
> [#1124](https://github.com/IHP-GmbH/IHP-Open-PDK/pull/1124), head `ab1510c`), so
> `ihp-sg13cmos5l/`, `ihp-sg13g2/` and `ihp-common/` now sit in one tree under one
> commit pin. That is not housekeeping: the overlay's 528 symlinks point back into
> the base with **relative** paths (`../../ihp-sg13g2/...`), so it only resolves when
> base and overlay are siblings under one root — which upstream's own instructions
> below already worked around by hand. This mirror's daily sync is **disabled**; it is
> kept read-only for provenance and will not track upstream any further.

# IHP SG13CMOS5L PDK (M1-M4-TM1 stack)
> [!WARNING]
> This repo is meant to be used **only** as a temporary storage during the development of the `build/compile` migration script for the sg13 cmos5l PDK.

## How to use it during development stage
```bash
git clone --branch dev --recurse-submodules https://github.com/IHP-GmbH/IHP-Open-PDK.git
cd IHP-Open-PDK
git clone https://github.com/IHP-GmbH/ihp-sg13cmos5l.git
```
You're done! Now return to your working directory and switch between PDKs changing the `$PDK` env variable to `ihp-sg13cmos5l`.
Note: for general configuration settings review the IHP-Open-PDK [documentation](https://ihp-open-pdk-docs.readthedocs.io/en/latest).

# 도수 후 수심 계산기

수평 직사각 수로의 운동량 보존식으로 상류 사류에 대응하는 도수 후 수심을 계산합니다.

- ID: E135
- App: https://nanalab.kr/eng-hydraulic-jump/
- Repository: https://github.com/NaNaCompany/eng-hydraulic-jump
- Formula: Fr₁ = V₁/√(gy₁); y₂ = y₁[√(1+8Fr₁²)−1]/2

## Model and data

폭이 일정한 수평 직사각 수로이며 도수 양쪽 단면의 압력은 정수압 분포입니다. 마찰·외력이 도수 운동량 수지에 미치는 영향은 무시합니다. 도수 전 Fr₁ > 1이 필요합니다. 실제 도수 위치나 안정성은 하류 수심 등 추가 조건에 달려 있습니다.

Inputs normalize to SI. Repeated-input models support adding/removing actual input rows. Calculations, finite-number checks and physical-domain checks run locally; no external property database or solver API is used.

## Validation

Run node --test tests/*.test.mjs and python scripts/build-locales.py --check. tests/reference.json contains independently computed high-precision default and boundary references. The source notices distinguish original MIT work from citation-only external references.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.

# Data sources and licensing notes

The `supplemental_v1` training and validation splits combine records derived
from the following research datasets. Labels and metadata in the released
JSONL files are transformations for the S2E-AL experiments; copyright in the
underlying text remains with the original authors and data providers.

| Source | Upstream project | License information found in the upstream dataset card |
|---|---|---|
| CHEAT | CHEAT AI-text corpus | ODC-By |
| HC3 | [Hello-SimpleAI/HC3](https://github.com/Hello-SimpleAI/chatgpt-comparison-detection) | CC BY-SA 4.0, subject to stricter licenses of incorporated source datasets |
| HC3 Plus | HC3 Plus dataset | No explicit license was recorded in the downloaded dataset card; users must verify the current upstream terms |
| LLMTrace | [LLMTrace](https://sweetdream779.github.io/LLMTrace-info/) | Apache-2.0 |
| RAID | [liamdugan/raid](https://github.com/liamdugan/raid) | MIT (as stated by the downloaded dataset card) |
| Ghostbuster | [vivek3141/ghostbuster-data](https://github.com/vivek3141/ghostbuster-data) | CC BY 3.0 |
| M4GT-Bench | [mbzuai-nlp/M4GT-Bench](https://github.com/mbzuai-nlp/M4GT-Bench) | No explicit license was recorded in the downloaded README; users must verify the current upstream terms |

Important notes:

- The official unlabeled RAID `test.csv` is not included and was not assigned
  synthetic labels. RAID-derived training records come from labeled upstream
  data.
- The held-out S2E-AL test split is not included in this release.
- XSum is used as an unseen-domain evaluation set and is not included in the
  released training pool.
- Each user is responsible for complying with the licenses and terms of all
  upstream datasets, including licenses inherited from their original source
  corpora.
- The manifest contains SHA256 hashes for integrity and reproducibility.

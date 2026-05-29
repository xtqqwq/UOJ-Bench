# UOJ-Bench

Official repository for the paper **"Beyond Problem Solving: UOJ-Bench for Evaluating Code Generation, Hacking, and Repair in Competitive Programming"** (ICML 2026).

<p align="center">
  <a href="https://xtqqwq.github.io/UOJ-Bench/">🏠 Leaderboard</a> •
  <a href="https://anonymous.4open.science/r/UOJ-Bench-7DE3">📄 Paper</a> •
  <a href="https://uoj.ac">⚖️ UOJ</a> •
  <a href="https://github.com/xtqqwq/UOJ-Bench">💻 GitHub</a>
</p>

## Introduction

UOJ-Bench evaluates large language models on competitive programming beyond code generation alone. Built from real submissions on the [Universal Online Judge (UOJ)](https://uoj.ac) and judged through UOJ’s native infrastructure, the benchmark covers three tasks:

- **Code generation** — solve problems from statements (672 problems).
- **Code hacking** — synthesize counter-examples for buggy submissions (Easy: overt errors; Hard: community hacks).
- **Code repair** — minimal patches that fix submissions under a similarity constraint (Easy / Hard).

Results are reported with **Pass@1** under direct (one-shot) evaluation. See the paper for test-time scaling, zero-day hacking, and contamination analyses.

## Leaderboard

Interactive results for all models and tasks:

**[https://xtqqwq.github.io/UOJ-Bench/](https://xtqqwq.github.io/UOJ-Bench/)**

Scores are loaded from [`leaderboard.json`](leaderboard.json) (Tables 2–3 in the paper). To update numbers, edit that file and redeploy Pages.

## Repository layout

| Path | Description |
|------|-------------|
| [`index.html`](index.html) | Leaderboard site (GitHub Pages) |
| [`leaderboard.json`](leaderboard.json) | Model scores and metric labels |
| [`styles.css`](styles.css) | Site styles |

Evaluation code and datasets will be released with the paper; this repo currently hosts the public leaderboard.

## Local preview

`fetch()` requires HTTP. From this directory:

```bash
python3 -m http.server 8080
```

Open [http://127.0.0.1:8080/](http://127.0.0.1:8080/).

## GitHub Pages

1. Push this repository to GitHub.
2. **Settings → Pages → Build and deployment**.
3. Source: deploy from branch **`main`**, folder **`/`** (root) or **`/docs`** if the repo root is the parent project—use the folder that contains `index.html`.
4. Site URL: `https://<user>.github.io/<repository>/`

## Citation

If you use UOJ-Bench in your work, please cite:

```bibtex
@inproceedings{xu2026uojbench,
  title     = {Beyond Problem Solving: {UOJ-Bench} for Evaluating Code Generation, Hacking, and Repair in Competitive Programming},
  author    = {Xu, Tingqiang and Zhou, Hangrui and Cai, Tianle and Gu, Alex and Lyu, Kaifeng},
  booktitle = {Proceedings of the International Conference on Machine Learning},
  year      = {2026},
  note      = {PMLR 306},
}
```

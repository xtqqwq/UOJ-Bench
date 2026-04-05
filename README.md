# UOJ-Bench site (GitHub Pages)

Static leaderboard for **Code generation** (one metric), **Code hacking** (Easy / Hard), and **Code repair** (Easy / Hard).

## Enable GitHub Pages

1. Push this repository to GitHub.
2. Open **Settings → Pages → Build and deployment**.
3. Under **Source**, choose **Deploy from a branch**.
4. Select your default branch and folder **`/docs`**, then save.

The site will be available at `https://<user>.github.io/<repository>/` (project Pages). Paths in `index.html` use relative URLs so assets resolve correctly.

## Update results

Edit [`leaderboard.json`](leaderboard.json):

- **`models`**: each entry has `model`, `generation`, `hacking.easy` / `hacking.hard`, `repair.easy` / `repair.hard` (numbers align with your paper tables).
- **`metricLabels`**: strings used as table headers so labels match the paper (e.g. Pass@1 vs. success rate).
- **`paperUrl`**: link shown in the hero (optional; omit or set `null` to hide).
- **`repoUrl`**: your GitHub repo URL for the footer link (optional).

## Local preview

`fetch()` requires HTTP; opening `index.html` as a file will show the error banner. From this directory run:

```bash
python3 -m http.server 8080
```

Then open `http://127.0.0.1:8080/`.

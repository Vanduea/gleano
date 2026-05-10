# APK downloads

Git repositories are a poor place for large binaries: clones become slow, every APK revision bloats history, and GitHub warns above ~50 MB.

**Recommended:** attach each build as an asset on [GitHub Releases](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository).

## Steps

1. Push your `gleano-website` repo **without** the `.apk` file (this folder ignores `*.apk` via `.gitignore`).
2. In your **app** repo (or the same repo), open **Releases** → **Draft a new release**.
3. Tag e.g. `v1.0.0`, upload `gleano-1.0.0.apk` under **Assets**, publish.
4. This site’s `index.html` is already set to `https://github.com/Vanduea/gleano/releases/latest` for download buttons.

After that, **Download** buttons point at:

`https://github.com/<owner>/<repo>/releases/latest`

Users tap **Assets** on that page and download the APK. No heavy file lives in the Pages branch.

## Optional: one-tap direct download URL

If the uploaded asset is named exactly `gleano-1.0.0.apk`:

`https://github.com/<owner>/<repo>/releases/download/v1.0.0/gleano-1.0.0.apk`

You can use that as `href` if you prefer a single click instead of opening the release page.

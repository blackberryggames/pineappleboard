# 🎵 Soundboard

A minimal, beautiful soundboard hosted entirely on GitHub Pages. Upload audio files via the web UI — they commit directly to this repo's `/audios/` folder via the GitHub API and are instantly playable at:

```
https://YOUR_USERNAME.github.io/YOUR_REPO/audios/filename.mp3
```

## Setup

1. **Create a public GitHub repo** (this one)
2. **Enable GitHub Pages**: Settings → Pages → Source: Deploy from branch → `main` / `/(root)`
3. **Get a Personal Access Token**: github.com/settings/tokens → New fine-grained token → Contents: Read & Write on this repo
4. **Open your site** and fill in username, repo name, and token in the Settings panel
5. **Upload sounds** by dragging audio files onto the upload zone

## File structure

```
/
├── index.html       ← The soundboard UI
├── .nojekyll        ← Tells GitHub Pages not to use Jekyll
├── README.md
└── audios/          ← Created automatically on first upload
    ├── aura.mp3
    └── ...
```

## Notes

- Your token is stored only in your browser's localStorage
- Audio files are served from `raw.githubusercontent.com` for playback
- The `✕` button on a card removes it from the board locally; to delete from GitHub, remove the file from the repo manually
- Supports MP3, WAV, OGG, FLAC, M4A, AAC, OPUS

## License

MIT

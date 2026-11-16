# news-digest-config

Settings for [news-digest](https://github.com/Porpused15/news-digest), kept apart from the
code so the companion app's token can change settings but never the code that runs with
the digest's secrets.

- `config.json` — send hour, language, look-back, email on/off and grouping, and the feed
  list. Read by the digest workflow at the start of each run; edited by the app.
- `.github/workflows/send-now.yml` — the app's "Send digest now" button starts this, and it
  starts the digest run in the main repo.

## Tokens

| Token | Where | Access |
|---|---|---|
| App token | pasted into the app | **this repo only**: Contents read/write, Actions read/write |
| `DIGEST_DISPATCH_TOKEN` | secret in this repo | **news-digest only**: Actions read/write |

# contrib-mirror-BuildPeer

Destination repository for [contrib-mirror](https://github.com/MikeAlvarado/contrib-mirror). The workflow in `.github/workflows/mirror.yml` runs once a day, reads the public contribution graph of the source account, and adds one commit per contribution to this repository, so a day with three contributions gets three commits. Only dates are stored, one line per mirrored contribution in `log.md`. Nothing else from the source account is copied.

There is nothing to configure. The workflow looks back a full year on every run and skips contributions already present in `log.md`, so it backfills itself on the first run and stays current afterwards. It can also be started by hand from the Actions tab.

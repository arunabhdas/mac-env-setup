~~~
==> brew reinstall postgresql
==> Downloading https://ghcr.io/v2/homebrew/core/postgresql/manifests/14.1_1
Already downloaded: /Users/coder/Library/Caches/Homebrew/downloads/34e850b9c47867f84334b48fe844f7a171369d777b5c118a4119297f7c215147--postgresql-14.1_1.bottle_manifest.json
==> Downloading https://ghcr.io/v2/homebrew/core/postgresql/blobs/sha256:6e6f3099ad1e64fbdc9dff2152c33a2f01743d2010330bcb34cefe13052fa228
Already downloaded: /Users/coder/Library/Caches/Homebrew/downloads/eacd586861a249595e1620030d938750a4783a3f3b3f7f4a49f3919cb0255d9e--postgresql--14.1_1.arm64_monterey.bottle.tar.gz
==> Reinstalling postgresql 
==> Pouring postgresql--14.1_1.arm64_monterey.bottle.tar.gz
==> Caveats
To migrate existing data from a previous major version of PostgreSQL run:
  brew postgresql-upgrade-database

This formula has created a default database cluster with:
  initdb --locale=C -E UTF-8 /opt/homebrew/var/postgres
For more details, read:
  https://www.postgresql.org/docs/14/app-initdb.html

To restart postgresql after an upgrade:
  brew services restart postgresql
Or, if you don't want/need a background service you can just run:
  /opt/homebrew/opt/postgresql/bin/postgres -D /opt/homebrew/var/postgres
==> Summary
🍺  /opt/homebrew/Cellar/postgresql/14.1_1: 3,304 files, 44.5MB
==> Running `brew cleanup postgresql`...
Disable this behaviour by setting HOMEBREW_NO_INSTALL_CLEANUP.
Hide these hints with HOMEBREW_NO_ENV_HINTS (see `man brew`).
~~~

brew postgresql-upgrade-database

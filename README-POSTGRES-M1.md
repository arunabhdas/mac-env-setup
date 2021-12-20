==> brew reinstall postgresql
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

==> brew postgresql-upgrade-database


```
==> brew postgresql-upgrade-database
==> brew install postgresql@13
==> Downloading https://ghcr.io/v2/homebrew/core/postgresql/13/manifests/13.5_1-1
######################################################################## 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/postgresql/13/blobs/sha256:a84101063f387e69e80296c938f34407a5502eb29281a5684da0ea6de37457eb
==> Downloading from https://pkg-containers.githubusercontent.com/ghcr1/blobs/sha256:a84101063f387e69e80296c938f34407a5502eb29281a5684da0ea6de37457eb?se=2021-12-20T19%3A45%3A00Z&sig=cpsATLgT8uQaip0gAVl3I%2FmEBiCPBEN8FxvKOAt7ZY8%3D&sp=r&spr=https&sr=b&sv=2019-12-12
######################################################################## 100.0%
==> Pouring postgresql@13--13.5_1.arm64_monterey.bottle.1.tar.gz
==> /opt/homebrew/Cellar/postgresql@13/13.5_1/bin/initdb --locale=C -E UTF-8 /opt/homebrew/var/postgresql@13
==> Caveats
Previous versions of this formula used the same data directory as
the regular PostgreSQL formula. This causes a conflict if you
try to use both at the same time.

In order to avoid this conflict, you should make sure that the
postgresql@13 data directory is located at:
  /opt/homebrew/var/postgresql@13

This formula has created a default database cluster with:
  initdb --locale=C -E UTF-8 /opt/homebrew/var/postgresql@13
For more details, read:
  https://www.postgresql.org/docs/13/app-initdb.html

postgresql@13 is keg-only, which means it was not symlinked into /opt/homebrew,
because this is an alternate version of another formula.

If you need to have postgresql@13 first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/postgresql@13/bin:$PATH"' >> /Users/coder/.bash_profile

For compilers to find postgresql@13 you may need to set:
  export LDFLAGS="-L/opt/homebrew/opt/postgresql@13/lib"
  export CPPFLAGS="-I/opt/homebrew/opt/postgresql@13/include"

For pkg-config to find postgresql@13 you may need to set:
  export PKG_CONFIG_PATH="/opt/homebrew/opt/postgresql@13/lib/pkgconfig"


To restart postgresql@13 after an upgrade:
  brew services restart postgresql@13
Or, if you don't want/need a background service you can just run:
  /opt/homebrew/opt/postgresql@13/bin/postgres -D /opt/homebrew/var/postgresql@13
==> Summary
🍺  /opt/homebrew/Cellar/postgresql@13/13.5_1: 3,233 files, 42.3MB
==> Running `brew cleanup postgresql@13`...
Disable this behaviour by setting HOMEBREW_NO_INSTALL_CLEANUP.
Hide these hints with HOMEBREW_NO_ENV_HINTS (see `man brew`).
==> Upgrading postgresql data from 13 to 14...
waiting for server to start....2021-12-20 14:38:22.503 EST [7017] LOG:  starting PostgreSQL 13.5 on arm-apple-darwin21.1.0, compiled by Apple clang version 13.0.0 (clang-1300.0.29.3), 64-bit
2021-12-20 14:38:22.506 EST [7017] LOG:  listening on IPv6 address "::1", port 5432
2021-12-20 14:38:22.506 EST [7017] LOG:  listening on IPv4 address "127.0.0.1", port 5432
2021-12-20 14:38:22.506 EST [7017] LOG:  listening on Unix socket "/tmp/.s.PGSQL.5432"
2021-12-20 14:38:22.510 EST [7018] LOG:  database system was shut down at 2021-08-24 15:01:22 EDT
2021-12-20 14:38:22.515 EST [7017] LOG:  database system is ready to accept connections
 done
server started
waiting for server to shut down....2021-12-20 14:38:22.914 EST [7017] LOG:  received fast shutdown request
2021-12-20 14:38:22.914 EST [7017] LOG:  aborting any active transactions
2021-12-20 14:38:22.915 EST [7017] LOG:  background worker "logical replication launcher" (PID 7024) exited with exit code 1
2021-12-20 14:38:22.915 EST [7019] LOG:  shutting down
2021-12-20 14:38:22.919 EST [7017] LOG:  database system is shut down
 done
server stopped
==> Moving postgresql data from /opt/homebrew/var/postgres to /opt/homebrew/var/postgres.old...
==> Creating database...
The files belonging to this database system will be owned by user "coder".
This user must also own the server process.

The database cluster will be initialized with locale "C".
The default text search configuration will be set to "english".

Data page checksums are disabled.

fixing permissions on existing directory /opt/homebrew/var/postgres ... ok
creating subdirectories ... ok
selecting dynamic shared memory implementation ... posix
selecting default max_connections ... 100
selecting default shared_buffers ... 128MB
selecting default time zone ... America/Toronto
creating configuration files ... ok
running bootstrap script ... ok
performing post-bootstrap initialization ... ok
syncing data to disk ... ok

initdb: warning: enabling "trust" authentication for local connections
You can change this by editing pg_hba.conf or using the option -A, or
--auth-local and --auth-host, the next time you run initdb.

Success. You can now start the database server using:

    /opt/homebrew/opt/postgresql/bin/pg_ctl -D /opt/homebrew/var/postgres -l logfile start

==> Migrating and upgrading data...
Performing Consistency Checks
-----------------------------
Checking cluster versions                                   ok
Checking database user is the install user                  ok
Checking database connection settings                       ok
Checking for prepared transactions                          ok
Checking for system-defined composite types in user tables  ok
Checking for reg* data types in user tables                 ok
Checking for contrib/isn with bigint-passing mismatch       ok
Checking for user-defined encoding conversions              ok
Checking for user-defined postfix operators                 ok
Creating dump of global objects                             ok
Creating dump of database schemas
                                                            ok
Checking for presence of required libraries                 ok
Checking database user is the install user                  ok
Checking for prepared transactions                          ok
Checking for new cluster tablespace directories             ok

If pg_upgrade fails after this point, you must re-initdb the
new cluster before continuing.

Performing Upgrade
------------------
Analyzing all rows in the new cluster                       ok
Freezing all rows in the new cluster                        ok
Deleting files from new pg_xact                             ok
Copying old pg_xact to new server                           ok
Setting oldest XID for new cluster                          ok
Setting next transaction ID and epoch for new cluster       ok
Deleting files from new pg_multixact/offsets                ok
Copying old pg_multixact/offsets to new server              ok
Deleting files from new pg_multixact/members                ok
Copying old pg_multixact/members to new server              ok
Setting next multixact ID and offset for new cluster        ok
Resetting WAL archives                                      ok
Setting frozenxid and minmxid counters in new cluster       ok
Restoring global objects in the new cluster                 ok
Restoring database schemas in the new cluster
                                                            ok
Copying user relation files
                                                            ok
Setting next OID for new cluster                            ok
Sync data directory to disk                                 ok
Creating script to delete old cluster                       ok
Checking for extension updates                              ok

Upgrade Complete
----------------
Optimizer statistics are not transferred by pg_upgrade.
Once you start the new server, consider running:
    /opt/homebrew/opt/postgresql/bin/vacuumdb --all --analyze-in-stages

Running this script will delete the old cluster's data files:
    ./delete_old_cluster.sh
==> Upgraded postgresql data from 13 to 14!
==> Your postgresql 13 data remains at /opt/homebrew/var/postgres.old
```

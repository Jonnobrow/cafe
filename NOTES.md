## Major DB Upgrades

Ref: https://cloudnative-pg.io/docs/1.29/postgres_upgrades#offline-in-place-major-upgrades

1. `task kubernetes:postgres-suspend`

- Note: This suspends flux for postgres labelled things, and scales to 0

2. Update image and serverName in: [postgres.yaml](./kubernetes/apps/database/cloudnative-pg/cluster/postgres.yaml)

3. Wait for update to complete

4. `task kubernetes:postgres-resume`

# Argus tracing migration

1. Go to `dwg-production` and stop prometheus and node-exporter. Those containers will not be used anymore: `docker compose down -v prometheus node-exporter`
2. Update repo URL: `git remote set-url origin [https://github.com/joyutils/dwg-production.git](https://github.com/joyutils/dwg-production.git)`
3. Fetch latest repo changes: `git pull origin main`
4. Modify `.env`:
    1. Change `ENABLE_TELEMETRY` to `yes`
    2. Add `ELASTIC_URL=https://elastic.joyutils.org:443`
    3. Add `ELASTIC_USERNAME` and `ELASTIC_PASSWORD` - use the same values as in distributor config
    4. Add `NODE_ID` - use the same value as `id` in distributor config
5. Modify you distributor config:
    1. Remove `id` - this is now passed via env variable
    2. In `logs.elastic` section leave only `level` field. Other values will be passed via env:
    
    ```yaml
    elastic:
        level: http
    ```
    
6. Stop services that need to update:
    1. `docker compose down graphql-server`
    2. `docker compose down distributor`
7. Start everything:
    1. `docker compose up -d collector`
    2. `docker compose up -d metricbeat`
    3. `docker compose up -d graphql-server`
    4. `docker compose up -d distributor`
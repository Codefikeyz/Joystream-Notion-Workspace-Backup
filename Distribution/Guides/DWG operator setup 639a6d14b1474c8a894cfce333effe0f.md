# DWG operator setup

## Basic services

Once the server has been confirmed with me and you have access:

1. Clone [https://github.com/joyutils/dwg-production](https://github.com/joyutils/dwg-production) and read readme
2. Adjust .env as necessary, good idea to use `PROCESSOR_INDEXER_GATEWAY=https://mainnet-rpc-1.joystream.org/query-node/indexer/graphql` so your processor syncs faster. Remember to set `ELASTIC_USERNAME` and `ELASTIC_PASSWORD`
3. Start services from readme
4. Confirm processor is syncing

---

## Distribution node

Once you have:

1. processor sync in progress
2. collector and metricbeat up
3. caddy up and online

It’s time to prepare your distributor config, accept bucket invitations and set metadata. [https://github.com/joyutils/dwg-production/blob/main/docs/DISTRIBUTOR.md](https://github.com/joyutils/dwg-production/blob/main/docs/DISTRIBUTOR.md) will be very helpful!

1. Adjust following values from example config:
    1. Set `id` as you please. You can see current ones here: [https://monitoring.joyutils.org/operator-logs](https://monitoring.joyutils.org/operator-logs)
    2. Your QN is not synced yet so use external for now: `endpoints.queryNode`: `https://query.joystream.org/graphql`
    3. Same with your Joystream node: `endpoints.joystreamNodeWs`: `wss://rpc.joystream.org`
    4. Uncomment full `logs.elastic` section and supply with your credentials
    5. Adjust `limits.storage` - the higher the better, but you need to reserve at least 200GB for chain+QN data and 100GB for system.
    6. Change `operatorApi.hmacSecret` to a long randomized string.
    7. Set your `workerId`
    8. Also make sure your role key exported as JSON is at path specified in `keys.keyfile`. `/keystore` mounted inside container maps to `DISTRIBUTOR_KEYSTORE_VOLUME` in .env
2. Next you will need to accept bucket invitation I’ve sent, check `Accepting invitation` in linked doc, use your own bucket and worker IDs.
3. Lastly, you need to set your on-chain operator metadata. This is also shown in the doc. You can find my metadata.json here: [https://gist.github.com/kdembler/d0308d33a2c722826259491fb9eb2c12](https://gist.github.com/kdembler/d0308d33a2c722826259491fb9eb2c12) Adjust for yourself.
4. Now you should be good to launch your `distributor` container. Check the logs to confirm no errors and check /distributor/api/v1/status. Initial sync may take even 10-15 minutes so give it some time.
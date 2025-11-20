# Resetting WG debt

Illustrates how to reset WG debt, particularly the distribution working group debt. The debt amount displayed in pioneer is the cumulative sum of each `missed_reward` for each worker.

The missed reward is increased when the WG budget is not sufficient in order to pay the worker the reward per block at the beginning each reward cycle. 
The solution is to fire and hire each worker. `distId` denotes the distribution bucket id the `oldId` worker is serving

<aside>
💡 **WORKERS SHOULD CARRY OUT ONLY STEPS WITH ORANGE BACKGROUND** (lead will take care of the rest)

</aside>

<aside>
💡 **STEPS SHOULD BE SERIALIZED TO HAVE AT MOST 1 OPERATOR NON DISTRIBUTING AT EACH TIME**

</aside>

### 1️⃣ Prepare new worker application

- who: Lead
- platform: Pioneer
- Application title: “Re-hire distribution operator `<MEMBER_HANDLE>` / `<MEMBER_ID>` (or some other member identifier for the previous worker

### 2️⃣ Mark distribution bucket `distId` as non distributing

- who: Lead
- platform: Polkadot-js

### 3️⃣ Remove distribution worker `oldId` operator

- who: Lead
- platform: Polkadot-js

Terminating the role removes all worker info from chain, including `missed_reward` thus decreasing the budget debt

### 4️⃣ Terminate worker `oldId` for operator

- who: Lead
- platform: Polkadot-js

### 5️⃣ Member should apply to previous application

- who: Worker
- platform: Pioneer
- **Caveat: use the same role account as your old role, to simplify the bucket invitation process**

### 6️⃣ Hire worker again under `newId`

- who: Lead
- platform: Polkadot-js

### 7️⃣ Invite worker `newId` for distribution bucket `distId`

- who: Lead
- platform: Polkadot-js

### 8️⃣ Distribution Worker `newId` should accept the invitation

<aside>
💡 **WAIT FOR PERMISSION FROM THE LEAD BEFORE PROCEEDING**

</aside>

- who: Worker
- platform: argus cli
- steps:
    1. Bring down distributor container if running `docker-compose down -v distributor`
    2. If you haven’t update your `docker-compose.yml` recently this is a good moment in order to select the latest argus release (you can copy the configuration below or just update the `image` field to `joystream/distributor-node:latest`)
        
        ```yaml
         distributor:
            image: joystream/distributor-node:latest
            container_name: distributor
            restart: unless-stopped
            volumes:
              - ${DISTRIBUTOR_KEYSTORE_VOLUME}:/keystore
              - ${DISTRIBUTOR_DATA_VOLUME}:/data
              - ${DISTRIBUTOR_CACHE_VOLUME}:/cache
              - ${DISTRIBUTOR_LOGS_VOLUME}:/logs
              - ${DISTRIBUTOR_SCRATCH_VOLUME}:/scratch
              - ${DISTRIBUTOR_CONFIG_VOLUME}:/joystream/distributor-node/config.yml:ro
              - ./runners/distributor.sh:/joystream/distributor-node/runner.sh:ro
            working_dir: /joystream/distributor-node
            ports:
              - 127.0.0.1:3334:3334 # Public API
              - 127.0.0.1:3335:3335 # Private node operator API
            environment:
              ENABLE_TELEMETRY: ${ENABLE_TELEMETRY:-no}
              OTEL_APPLICATION: distributor-node
              OTEL_EXPORTER_OTLP_ENDPOINT: <http://collector:4318>
              OTEL_RESOURCE_ATTRIBUTES: service.name=argus,deployment.environment=production
              NODE_ENV: production
              JOYSTREAM_DISTRIBUTOR__ID: ${NODE_ID}
              JOYSTREAM_DISTRIBUTOR__LOGS__ELASTIC__ENDPOINT: ${ELASTIC_URL}
              JOYSTREAM_DISTRIBUTOR__LOGS__ELASTIC__AUTH__USERNAME: ${ELASTIC_USERNAME}
              JOYSTREAM_DISTRIBUTOR__LOGS__ELASTIC__AUTH__PASSWORD: ${ELASTIC_PASSWORD}
            entrypoint: ["/joystream/distributor-node/runner.sh"]
            command: ["start"]
        
        ```
        
    3. change the `distributor/config/config.yml` `workerId` field to the `newId` provided
    4. start distribution node `docker compose up -d distributor`
    5. accept invitation:
        
        ```
        docker compose run --rm distributor \\\\
          operator:accept-invitation -B <DIST_ID> -w <NEW_ID>
        
        ```
        

### 9️⃣ Distribution Worker `newId` should set the new metadata

- who: Worker
- platform: argus cli

Say you have the metadata file in your home directory `~/metadata.json` 

```
docker compose run --rm \\\\
  -v ~/metadata.json:/metadata.json \\\\
  distributor operator:set-metadata -B <DIST_ID> -w <NEW_ID> --input /metadata.json

```

### 🔟 Adjust block reward if necessary

- who: Lead
- platform: pioneer

If the salary for the current term has already been paid, because the reward per block amount was too high, then the new reward per block should be `0` until the end of the term
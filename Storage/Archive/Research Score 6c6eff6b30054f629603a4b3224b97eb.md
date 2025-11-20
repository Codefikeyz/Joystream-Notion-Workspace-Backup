# Research Score

# Task

**Research Logging**

To evaluate a system like this, we need to make sure the individual node logs are available, and useful.

**`DEFAULT_LOGGING`** Review what is currently being logged by a storage node, for each configurable `log-level`. Describe what information it provides, and in what way it can be used to improve the data in the current report, or what new statistics can be derived from it.

# Summary

All logging messages are pretty straightforward. It seems that the most important log-levels for the decision making by the Storage Lead or Storage Deputy Lead are

- Error

```bash
error:	Sync - fetching data error for [https://whitesocks.ru/storage/api/v1/files/13234:](https://whitesocks.ru/storage/api/v1/files/13234:) Error: Invalid file hash. Expected: gWE4d89jRT8CF7VQjFv5hi32dfhsVmbXnU53fT4B9dvYg3 - real: gWA8ejdyVhcaiwBSc9AqtN8nQidkDJinZEFL498TQRxrR2
error:	Sync - unexpected status code(404) for [https://ru.joystreamstats.live/storage/api/v1/files/14260](https://ru.joystreamstats.live/storage/api/v1/files/14260)
```

All these errors are critical and should be investigated asap.

- Warn

```bash
warn:	Sync - cannot get operator URLs for 12847
```

This will give Lead a clue about which objects are absent.

- Debug

```bash
debug:	Sync - downloading file: [https://whitesocks.ru/storage/api/v1/files/13234](https://whitesocks.ru/storage/api/v1/files/13234) to /root/.joystream-storage ....
```

This will help the Lead to understand whether objects are syncing smoothly across different Storage node or not. 

All in all, I would suggest that ERROR and WARN messages should be automatically reported by the Storage node operators on a daily basis, and then should be carefully investigated by the Storage Lead and Storage Deputy Lead.

# Log-Level: Examples

## Debug

```bash
debug:	Query - storageBucketsConnection
debug:	Query - storageBagsConnection
debug:	Query - storageBagsConnection
debug:	Query - storageBucketsConnection
debug:	Query - storageDataObjectsConnection
debug:	Query - storageDataObjectsConnection
debug:	Sync - downloading file: [https://ru.joystreamstats.live/storage/api/v1/files/13234](https://ru.joystreamstats.live/storage/api/v1/files/13234) to /root/.joystream-storage ....
debug:	Sync - downloading file: [https://ru.joystreamstats.live/storage/api/v1/files/13234](https://ru.joystreamstats.live/storage/api/v1/files/13234) to /root/js-storage/ ....
debug:	Sync - downloading file: [https://ru.joystreamstats.live/storage/api/v1/files/14260](https://ru.joystreamstats.live/storage/api/v1/files/14260) to /root/.joystream-storage ....
debug:	Sync - downloading file: [https://ru.joystreamstats.live/storage/api/v1/files/14260](https://ru.joystreamstats.live/storage/api/v1/files/14260) to /root/js-storage/ ....
debug:	Sync - downloading file: [https://whitesocks.ru/storage/api/v1/files/13234](https://whitesocks.ru/storage/api/v1/files/13234) to /root/.joystream-storage ....
debug:	Sync - downloading file: [https://whitesocks.ru/storage/api/v1/files/13234](https://whitesocks.ru/storage/api/v1/files/13234) to /root/js-storage/ ....
debug:	Sync - fetching available data for [https://ipfs.joystreamstats.live/storage/api/v1/state/data-objects](https://ipfs.joystreamstats.live/storage/api/v1/state/data-objects)
debug:	Sync - fetching available data for [https://joystream.godshunter.su/storage/api/v1/state/data-objects](https://joystream.godshunter.su/storage/api/v1/state/data-objects)
debug:	Sync - fetching available data for [https://joystream2.yyagi.cloud/storage/api/v1/state/data-objects](https://joystream2.yyagi.cloud/storage/api/v1/state/data-objects)
debug:	Sync - fetching available data for [https://jssp.cryptostarter.info/storage/api/v1/state/data-objects](https://jssp.cryptostarter.info/storage/api/v1/state/data-objects)
debug:	Sync - fetching available data for [https://ru.joystreamstats.live/storage/api/v1/state/data-objects](https://ru.joystreamstats.live/storage/api/v1/state/data-objects)
debug:	Sync - fetching available data for [https://whitesocks.ru/storage/api/v1/state/data-objects](https://whitesocks.ru/storage/api/v1/state/data-objects)
debug:	Sync - getting all storage buckets: offset = 0 limit = 1000
debug:	Sync - getting all storage buckets: offset = 0 limit = 1000
debug:	Sync - getting from cache available data for [https://ipfs.joystreamstats.live/storage/api/v1/state/data-objects](https://ipfs.joystreamstats.live/storage/api/v1/state/data-objects)
debug:	Sync - getting from cache available data for [https://joystream.godshunter.su/storage/api/v1/state/data-objects](https://joystream.godshunter.su/storage/api/v1/state/data-objects)
debug:	Sync - getting from cache available data for [https://joystream2.yyagi.cloud/storage/api/v1/state/data-objects](https://joystream2.yyagi.cloud/storage/api/v1/state/data-objects)
debug:	Sync - getting from cache available data for [https://jssp.cryptostarter.info/storage/api/v1/state/data-objects](https://jssp.cryptostarter.info/storage/api/v1/state/data-objects)
debug:	Sync - getting from cache available data for [https://ru.joystreamstats.live/storage/api/v1/state/data-objects](https://ru.joystreamstats.live/storage/api/v1/state/data-objects)
debug:	Sync - getting from cache available data for [https://whitesocks.ru/storage/api/v1/state/data-objects](https://whitesocks.ru/storage/api/v1/state/data-objects)
debug:	Sync - new objects: 0
debug:	Sync - new objects: 2
debug:	Sync - new objects: 4
debug:	Sync - obsolete objects: 1
debug:	Sync - obsolete objects: 19
debug:	Sync - obsolete objects: 5
debug:	Sync - obsolete objects: 7
debug:	Sync - preparing for download of: 12846 ....
debug:	Sync - preparing for download of: 12847 ....
debug:	Sync - preparing for download of: 12862 ....
debug:	Sync - preparing for download of: 12863 ....
debug:	Sync - preparing for download of: 13234 ....
debug:	Sync - preparing for download of: 14260 ....
debug:	Sync - random storage node URL was chosen [https://ipfs.joystreamstats.live/storage/](https://ipfs.joystreamstats.live/storage/)
debug:	Sync - random storage node URL was chosen [https://joystream.godshunter.su/storage/](https://joystream.godshunter.su/storage/)
debug:	Sync - random storage node URL was chosen [https://joystream2.yyagi.cloud/storage/](https://joystream2.yyagi.cloud/storage/)
debug:	Sync - random storage node URL was chosen [https://jssp.cryptostarter.info/storage/](https://jssp.cryptostarter.info/storage/)
debug:	Sync - random storage node URL was chosen [https://ru.joystreamstats.live/storage/](https://ru.joystreamstats.live/storage/)
debug:	Sync - random storage node URL was chosen [https://whitesocks.ru/storage/](https://whitesocks.ru/storage/)
debug:	Sync - started processing...
debug:	Sync - started processing...
```

## Error

```bash
error:	Sync - fetching data error for [https://ru.joystreamstats.live/storage/api/v1/files/13234:](https://ru.joystreamstats.live/storage/api/v1/files/13234:) Error: Invalid file hash. Expected: gWE4d89jRT8CF7VQjFv5hi32dfhsVmbXnU53fT4B9dvYg3 - real: gWA8ejdyVhcaiwBSc9AqtN8nQidkDJinZEFL498TQRxrR2
error:	Sync - fetching data error for [https://ru.joystreamstats.live/storage/api/v1/files/14260:](https://ru.joystreamstats.live/storage/api/v1/files/14260:) Error: Invalid file hash. Expected: gW36PcB5wH1NJfXjWMN2hygnx7aibmF9eJ91b8CrBGRCep - real: gWA8ejdyVhcaiwBSc9AqtN8nQidkDJinZEFL498TQRxrR2
error:	Sync - fetching data error for [https://whitesocks.ru/storage/api/v1/files/13234:](https://whitesocks.ru/storage/api/v1/files/13234:) Error: Invalid file hash. Expected: gWE4d89jRT8CF7VQjFv5hi32dfhsVmbXnU53fT4B9dvYg3 - real: gWA8ejdyVhcaiwBSc9AqtN8nQidkDJinZEFL498TQRxrR2
error:	Sync - unexpected status code(404) for [https://ru.joystreamstats.live/storage/api/v1/files/13234](https://ru.joystreamstats.live/storage/api/v1/files/13234)
error:	Sync - unexpected status code(404) for [https://ru.joystreamstats.live/storage/api/v1/files/14260](https://ru.joystreamstats.live/storage/api/v1/files/14260)
```

## Info

```bash
info:	Resume syncing....
info:	Resume syncing....
info:	Started syncing...
info:	Started syncing...
info:	Sync ended.
info:	Sync ended.
info:	Sync paused for 1 minute(s).
info:	Sync paused for 1 minute(s).
```

## Warn

```bash
warn:	Cleaning up file /root/.joystream-storage/temp/eac885e0-27a2-4ddb-90c6-b6a7a1de383b
warn:	Sync - cannot get operator URLs for 12846
warn:	Sync - cannot get operator URLs for 12847
warn:	Sync - cannot get operator URLs for 12862
warn:	Sync - cannot get operator URLs for 12863
```

## Not-specified-level

```bash
http:	HTTP  GET /api/v1/state/data
http:	HTTP  GET /api/v1/version
http:	HTTP GET /api/v1/files/13234
http:	HTTP GET /api/v1/state/data-objects
http:	HTTP GET /api/v1/version
http:	HTTP GET /asset/v0/5E99u78KHrxHrBUjCDqaYi7wnfvpVNDDM8DSkVu24REm9PYM
http:	HTTP GET /asset/v0/5ENdke3kfMTF8P1konRLieDDJyFVF2NKAZyfYPL1CAgYx9zX
http:	HTTP HEAD /api/v1/files/14440
http:	HTTP HEAD /api/v1/files/192
```
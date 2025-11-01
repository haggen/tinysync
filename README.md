# TinySync

> A public WebSocket synchronizer for [TinyBase](https://tinybase.org).

## Usage

Connect your clients to `wss://tinysync.crz.li/<channel>`, replacing `<channel>` with any valid, non-empty path. Any stores connected to the same channel will synchronize with each other in real time.

### Example

```js
const webSocket = new WebSocket("wss://tinysync.crz.li/example/room-1");
const store = createMergeableStore();
const synchronizer = await createWsSynchronizer(store, webSocket);

await synchronizer.startSync();
```

Read the [TinyBase documentation](https://tinybase.org/guides/synchronization/) for more details on synchronization.

## Legal

By using `wss://tinysync.crz.li`, you agree to be **lawful good**. We reserve the right to monitor, restrict, or terminate access at any time without notice. Your use of this service is at your own risk, and we are not liable for any damages or losses resulting from its use.

This project is not endorsed by or affiliated with TinyBase. It is provided as-is, without warranty of any kind, under the terms of the [Apache License, Version 2.0](./LICENSE.md).

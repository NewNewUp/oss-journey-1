# WebSockets drop; design the reconnect before the first deploy

Note: `notes/websocket-reconnect.md` — one of the debugging notes in this repository.

- Exponential backoff with jitter on reconnect, or a server restart synchronizes every client.
- Resync state after reconnect rather than replaying messages you missed.
- Heartbeats distinguish a dead connection from an idle one; proxies kill idle sockets in minutes.
- Auth tokens expire mid-socket; define the re-auth handshake before launch.

Written while the failure was fresh; the pattern outlives the project.

Related: see `notes/ten-pr-lessons.md` for the meta-lessons.

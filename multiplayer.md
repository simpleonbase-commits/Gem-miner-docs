# Multiplayer

Gem Miner supports real-time multiplayer powered by Cloudflare Durable Objects.

## How It Works

Multiple players can share the same world instance and see each other mining in real time. The server is **authoritative for gem positions** — preventing double-claiming of ore across sessions.

- See other players' wallets and positions in the world
- Ore claimed by one player is immediately removed for all others
- WebSocket-based real-time sync with low latency
- Server tracks: player positions, gem positions, wallet mappings, presence

## Social Dynamics

Multiplayer creates natural cooperation and competition:

- **Competition** — race other players to rare ore veins at depth
- **Coordination** — group up to take down Alpha goblins together
- **Risk** — other players can see you carrying unredeemed inventory

## Technical

The multiplayer backend runs as a single Cloudflare Durable Object instance per game room, providing shared state with global low-latency access.

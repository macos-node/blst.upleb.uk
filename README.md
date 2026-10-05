# blst.upleb.uk

> Nostr event rebroadcaster — push any event across an arbitrary relay list.

**Live**: <https://blst.upleb.uk>

## Stack

- [Vite](https://vitejs.dev/) + React 18 + TypeScript
- Tailwind CSS
- [nostr-tools](https://github.com/nbd-wtf/nostr-tools)
- lucide-react

## Nostr

- **Login**: NIP-07 (browser extension) + NIP-55 (Amber callback URI)
- `any kind` — user-selectable

Default target relay: `wss://git.upleb.uk` (the upleb GRASP relay).

## Develop

```bash
npm install
npm run dev
```

## Build + deploy

```bash
./deploy.sh
```

Builds, then rsyncs `dist/` to the webroot. The script names the server by an
SSH host alias (`upleb.uk` in `~/.ssh/config`), which carries the user, port and
key.

Server addresses and the nginx / SSL / DNS notes for the wider deployment live in the local `code_gh/macos-node/CLAUDE.md` (not pushed; this README is the public-facing summary).

---

_Sister repo on the other side: <https://github.com/adjmx/blst.fizx.uk>_

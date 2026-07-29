# Tarinoi for Unity — Quickstart

A minimal Unity 6 project that plays dialogue authored in
[Tarinoi](https://tarinoi.com), using the
[Tarinoi Unity package](https://github.com/tarinoi/tarinoi-unity-plugin).

Clone it, point it at your Tarinoi project, and press Play. If you would rather add
Tarinoi to a project you already have, install the package directly and follow its
[getting-started guide](https://github.com/tarinoi/tarinoi-unity-plugin/blob/main/Documentation~/getting-started.md).

Requires **Unity 6000.0** or newer.

> **Status: early development.** The package is still being built out and there is no
> tagged release yet.

## Running it

1. Clone this repository and open it in Unity 6.
2. **Project Settings → Tarinoi** — paste your project's documents endpoint into
   **API path**, then click **Set…** next to API token and paste a read token from your
   Tarinoi project's Integrations page.
3. **Tools → Tarinoi → Sync**.
4. **Tools → Tarinoi → Regenerate Bindings**.
5. Open `Assets/Tarinoi Quickstart.unity` and press Play.

You should get a list of every entry point in your content. Pick one and it plays.

If the list is empty, the Console will say why — the sync log and the troubleshooting
table in the package's getting-started guide cover the usual causes.

## What is in here

Almost nothing, deliberately. The scene holds a single GameObject with a
`TarinoiQuickstart` component; the interface is built at runtime by the package. That
keeps this repository about *using* Tarinoi rather than about a particular UI.

To register your own game's functions and variables, import the **Quickstart** sample
from the Package Manager and swap the component for the `MyQuickstart` it provides —
it has a `SetupBindings()` override showing where they go.

## Local development against the package

`Packages/manifest.json` refers to a sibling checkout:

```json
"com.tarinoi.unity": "file:../../tarinoi-unity-plugin"
```

Replace that with a version number to consume the published package instead — see the
package README for the registry entry.

## Not in version control

Three things are local to your checkout, and gitignored:

- `Assets/Resources/TarinoiSettings.asset` — points at a specific Tarinoi project.
- `Assets/Tarinoi/Generated/` — bindings generated from that project's content.
- `Assets/StreamingAssets/tarinoi/` — the exported content snapshot.

Your API token is never in the project at all: it lives outside it, so it cannot be
committed or shipped.

## License

MIT — see [`LICENSE.md`](LICENSE.md).

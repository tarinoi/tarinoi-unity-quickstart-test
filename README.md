# Tarinoi for Unity — Quickstart

A minimal Unity 6 project that demonstrates the
[Tarinoi dialogue package](https://github.com/tarinoi/tarinoi-unity-plugin): sync
authored dialogue content from Tarinoi, pick a starting point, and play it back.

If you want to see Tarinoi working with the least possible setup, start here. If you
want to add Tarinoi to a project you already have, install the package directly and
follow its getting-started guide instead.

Requires **Unity 6000.0** or newer.

> **Status: early development.** The package this project consumes is still being
> built out, and the end-to-end dialogue flow is not in place yet.

## Running it

1. Clone this repository and open it in Unity 6.
2. Set your project's documents endpoint in **Project Settings → Tarinoi**.
3. Save your API token via **Tools → Tarinoi → Set API token…**.
4. Run **Tools → Tarinoi → Sync**.
5. Press Play.

## How it consumes the package

During development this project references the package from a sibling checkout, via
`Packages/manifest.json`:

```json
"com.tarinoi.unity": "file:../../tarinoi-unity-plugin"
```

To use the published package instead, replace that line with a version number and add
the OpenUPM scoped registry — see the package README for the exact manifest entry.

## License

MIT — see [`LICENSE.md`](LICENSE.md).

# Awakened PoE Trade — 3.30 (Covens) build

This is [Awakened PoE Trade](https://github.com/SnosMe/awakened-poe-trade) by SnosMe with fixes for
Path of Exile 3.30 items that the official release doesn't handle yet. Hotkeys, settings and behaviour
are the same as the official app.

**Download:** grab `Awakened-PoE-Trade-Setup-*.exe` from the
[latest release](https://github.com/angad666/awakened-poe-trade-330/releases/latest) and run it.
Installing over the official app keeps your settings. Windows may show a SmartScreen warning
because the installer isn't code-signed: click *More info → Run anyway*.

### What's fixed for 3.30

- **Item Tier on unidentified items:** "Unidentified (Tier 4)" items are recognised again, and the
  search includes an *Unid. Tier* filter (on by default).
- **Chronicle of Atzoatl:** temple rooms are recognised again, with the Open/Obstructed tick boxes,
  including the renamed Cradle of Creation, Royal Forge and Grand Reactor rooms.
- **Viscera:** price checks now work and search by slot (head, torso, upper/lower limb) and implicit.
- **Uniques with skill names** such as "Trigger Level 10 Void Gaze…" are matched again (3.30 added an
  invisible character before skill names).
- **Frayed Thread** price checks, plus six uniques and a stat that the 3.30 data update dropped.
- **Facetor's Lens:** price checks work again (the item was missing from the data), and the search
  includes a *Stored Experience* filter so full and nearly empty lenses aren't priced together.

Also included from the official source, but not yet in an official release: twice-corrupted items,
rare-only mods and 9-mod maps, Thread/Atlas Drops map stats, and the *Not Catalysed* jewellery filter.

Not supported (same as the official app): Enshrouded items, because the trade site can't filter them
by their original unique.

Updates for this build come from this repository's releases, not the official one.

---

# ![Awakener's Orb](https://web.poecdn.com/image/Art/2DItems/Currency/TransferOrb.png) Awakened PoE Trade

[![](https://user-images.githubusercontent.com/4292308/153364874-dde23599-278c-4350-8d86-dadbc4b978b3.svg)](https://somsubhra.github.io/github-release-stats/?username=SnosMe&repository=awakened-poe-trade)
[![](https://user-images.githubusercontent.com/4292308/153364769-e4fe1e82-1bbc-46ac-8a3c-f5a98a5667cc.svg)](https://patreon.com/awakened_poe_trade)
[![](https://user-images.githubusercontent.com/4292308/153364565-7a545d26-e617-4a33-a919-ff90d8feda3d.svg)](https://github.com/SnosMe/awakened-poe-trade/issues/22)


➡ [Download for Windows & Linux](https://snosme.github.io/awakened-poe-trade/download) ⬅

## Tool showcase

| Gem | Rare | Unique | Currency |
|-----|------|--------|----------|
| ![](https://i.imgur.com/LTsH2DZ.png) | ![](https://i.imgur.com/2XL5Wl8.png) | ![](https://i.imgur.com/UTV6prE.png) | ![](https://i.imgur.com/dQ9Sns6.png) |

### Development

See [DEVELOPING.md](./DEVELOPING.md)

### Acknowledgments

- [libuiohook](https://github.com/kwhat/libuiohook)
- [RePoE](https://github.com/brather1ng/RePoE)
- [poeprices.info](https://www.poeprices.info/)
- [poe.ninja](https://poe.ninja/)

![](https://i.imgur.com/MATqhv7.png)

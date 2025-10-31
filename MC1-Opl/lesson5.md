# MC Reeks 1 Les 5

```template
player.onChat("luciferAan", function (hoogte, x, z) {
    steekLuciferAan(hoogte, x, z)
})
player.onChat("plaatsLucifer", function (hoogte, x, z) {
    builder.teleportTo(world(x, 0, z))
    if (hoogte < 3) {
        hoogte = 3
    }
    for (let index = 0; index < hoogte - 1; index++) {
        builder.place(PLANKS_BIRCH)
        builder.move(UP, 1)
    }
    builder.place(TNT)
})
function steekLuciferAan (hoogteRedstone: number, xRedstone: number, zRedstone: number) {
    loops.pause(100)
    builder.teleportTo(world(xRedstone, hoogteRedstone, zRedstone))
    builder.place(REDSTONE_BLOCK)
}

player.onChat("Knaltekst", function (Hoogte) {
    blocks.print(
    "BOEM",
    TNT,
    pos(0, Hoogte, 0),
    WEST
    )
    tekstAansteken(Hoogte)
})
function tekstAansteken (hoogteTekst: number) {
    builder.teleportTo(pos(0, hoogteTekst, 0))
    builder.place(REDSTONE_BLOCK)
}

```

```block
player.onChat("luciferAan", function (hoogte, x, z) {
    steekLuciferAan(hoogte, x, z)
})
player.onChat("plaatsLucifer", function (hoogte, x, z) {
    builder.teleportTo(world(x, 0, z))
    if (hoogte < 3) {
        hoogte = 3
    }
    for (let index = 0; index < hoogte - 1; index++) {
        builder.place(PLANKS_BIRCH)
        builder.move(UP, 1)
    }
    builder.place(TNT)
})
function steekLuciferAan (hoogteRedstone: number, xRedstone: number, zRedstone: number) {
    loops.pause(100)
    builder.teleportTo(world(xRedstone, hoogteRedstone, zRedstone))
    builder.place(REDSTONE_BLOCK)
}

player.onChat("Knaltekst", function (Hoogte) {
    blocks.print(
    "BOEM",
    TNT,
    pos(0, Hoogte, 0),
    WEST
    )
    tekstAansteken(Hoogte)
})
function tekstAansteken (hoogteTekst: number) {
    builder.teleportTo(pos(0, hoogteTekst, 0))
    builder.place(REDSTONE_BLOCK)
}

```

## Lucifer

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je een lucifer maakt.

[Klik hier om naar het leerplatform te gaan](https://leerplatform.codefever.be/).

![Lucifer](https://codefeverpublic.blob.core.windows.net/public-content/images/b7d2eb2b7c44f6e9cb261820635c36c2dbed83fb6f071d4f654c9b80065b1b13.png)

## Steek de lucifer aan

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je de lucifer aansteekt.

![Steek de lucifer aan](https://codefeverpublic.blob.core.windows.net/public-content/images/29c0bde5e45b6bba430550f4732003672637d7017cf5c9a287ae553c245cdc27.png)

## Lucifer met parameter

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je een lucifer met parameter maakt.

![Lucifer met parameter](https://codefeverpublic.blob.core.windows.net/public-content/images/c29f26ea646856daa0196bfecdaee3fa9ec9e5ced0d019cbde7e3234d7abb4c0.png)

## Knaltekst

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je knallende tekst maakt.

![Knaltekst](https://codefeverpublic.blob.core.windows.net/public-content/images/f5657213b96992928ad1e937ad082af73f068c7a5c46fe690f13f3f3ac5447ff.png)

# MC Reeks 1 Les 4

```template
player.onChat("floorIsLava", function () {})
player.onChat("bouwDouche", function () {})
player.onChat("bouwSpookhuis", function () {})
```

```block
player.onChat("floorIsLava", function () {
    while (true) {
        if (player.position().getValue(Axis.Y) <= 0) {
            blocks.fill(
            WATER,
            world(-9, -1, -9),
            world(9, -1, 9),
            FillOperation.Replace
            )
        } else {
            blocks.fill(
            LAVA,
            world(-9, -1, -9),
            world(9, -1, 9),
            FillOperation.Replace
            )
        }
    }
})

player.onChat("bouwDouche", function () {
    builder.teleportTo(world(10, -1, 10))
    builder.place(DIAMOND_BLOCK)
    builder.move(FORWARD, 1)
    for (let index = 0; index < 5; index++) {
        builder.move(UP, 1)
        builder.place(STONE)
    }
    builder.move(BACK, 1)
    builder.place(STONE)
    while (true) {
        if (blocks.testForBlock(DIAMOND_BLOCK, pos(0, -1, 0))) {
            blocks.place(WATER, world(10, 5, 10))
        } else {
            blocks.place(AIR, world(10, 5, 10))
        }
    }
})

player.onChat("zones", function () {
    blocks.fill(
    GOLD_BLOCK,
    pos(1, -1, 2),
    pos(2, -1, 3),
    FillOperation.Replace
    )
    blocks.fill(
    DIAMOND_BLOCK,
    pos(-1, -1, -2),
    pos(-2, -1, -3),
    FillOperation.Replace
    )
    while (true) {
        if (blocks.testForBlock(GOLD_BLOCK, pos(0, -1, 0))) {
            for (let index = 0; index < 20; index++) {
                mobs.spawn(BAT, pos(0, 2, 0))
            }
        } else if (blocks.testForBlock(DIAMOND_BLOCK, pos(0, -1, 0))) {
            blocks.fill(
            LAVA,
            pos(1, -1, 1),
            pos(2, -1, 2),
            FillOperation.Replace
            )
        }
    }
})
player.onChat("bouwSpookhuis", function () {
    blocks.fill(
    MANGROVE_WOOD,
    pos(10, -1, 10),
    pos(20, 5, 20),
    FillOperation.Hollow
    )
})

```

## The floor is lava

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je van de vloer lava maakt.

[Klik hier om naar het leerplatform te gaan](https://leerplatform.codefever.be/).

![The floor is lava](https://codefeverpublic.blob.core.windows.net/public-content/images/b2d985346f98d21e17bce8a52b49b89382e2ff3dc5de661b69f453defd35601e.png)

## Douche

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je een douche maakt.

![Douche](https://codefeverpublic.blob.core.windows.net/public-content/images/8f111f353a563910041270e0b32d9bd23aafddccbbd56a70759f6270aeab30ed.png)

## Spookhuis

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je een spookhuis maakt.

![Spookhuis](https://media.giphy.com/media/Yph6D7zPIVtIc/giphy.gif)

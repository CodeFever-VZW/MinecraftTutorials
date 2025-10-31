# MC Algemeen 1 Les 2

```template
player.onChat("serre", function () {
    builder.teleportTo(world(-5, 0, 5))
    for (let index = 0; index < 5; index++) {
        for (let index = 0; index < 4; index++) {
            for (let index = 0; index < 5; index++) {
                builder.place(GLASS)
                builder.move(FORWARD, 1)
            }
            builder.turn(RIGHT_TURN)
        }
        builder.move(UP, 1)
    }
})
player.onChat("toren", function () {
    builder.teleportTo(world(-10, 0, 10))
    for (let index = 0; index < 10; index++) {
        builder.place(MOSSY_STONE_BRICKS)
        builder.move(UP, 1)
    }
})
player.onChat("bank", function () {
    builder.teleportTo(world(7, 0, 5))
    builder.place(PLANKS_DARK_OAK)
    builder.move(LEFT, 1)
    builder.place(PLANKS_DARK_OAK)
    builder.move(FORWARD, 1)
    builder.place(PLANKS_DARK_OAK)
    builder.move(RIGHT, 1)
    builder.place(PLANKS_DARK_OAK)
    builder.move(UP, 1)
    builder.place(PLANKS_DARK_OAK)
    builder.move(LEFT, 1)
    builder.place(PLANKS_DARK_OAK)
})
player.onTravelled(WALK, function () {
    builder.teleportTo(player.position())
    builder.place(CORNFLOWER)
})
player.onChat("plaatsBomen", function () {
    builder.teleportTo(world(2, 0, 5))
    builder.place(DARK_OAK_SAPLING)
    builder.move(FORWARD, 1)
    builder.place(ACACIA_SAPLING)
    builder.move(FORWARD, 1)
    builder.place(DARK_OAK_SAPLING)
    builder.move(FORWARD, 1)
    builder.place(ACACIA_SAPLING)
})
player.onChat("torenGoud", function () {
    builder.teleportTo(world(4, 0, 5))
    builder.place(GOLD_BLOCK)
    builder.move(UP, 1)
    builder.place(GOLD_BLOCK)
    builder.move(UP, 1)
    builder.place(GOLD_BLOCK)
})
player.onChat("afsluiting", function () {
    builder.teleportTo(world(-12, 0, 15))
    for (let index = 0; index < 4; index++) {
        for (let index = 0; index < 20; index++) {
            builder.place(SPRUCE_FENCE)
            builder.move(FORWARD, 1)
        }
        builder.turn(RIGHT_TURN)
    }
})
```

```block
player.onChat("serre", function () {
    builder.teleportTo(world(-5, 0, 5))
    for (let index = 0; index < 5; index++) {
        for (let index = 0; index < 4; index++) {
            for (let index = 0; index < 5; index++) {
                builder.place(GLASS)
                builder.move(FORWARD, 1)
            }
            builder.turn(RIGHT_TURN)
        }
        builder.move(UP, 1)
    }
})
player.onChat("toren", function () {
    builder.teleportTo(world(-10, 0, 10))
    for (let index = 0; index < 10; index++) {
        builder.place(MOSSY_STONE_BRICKS)
        builder.move(UP, 1)
    }
})
player.onChat("bank", function () {
    builder.teleportTo(world(7, 0, 5))
    builder.place(PLANKS_DARK_OAK)
    builder.move(LEFT, 1)
    builder.place(PLANKS_DARK_OAK)
    builder.move(FORWARD, 1)
    builder.place(PLANKS_DARK_OAK)
    builder.move(RIGHT, 1)
    builder.place(PLANKS_DARK_OAK)
    builder.move(UP, 1)
    builder.place(PLANKS_DARK_OAK)
    builder.move(LEFT, 1)
    builder.place(PLANKS_DARK_OAK)
})
player.onTravelled(WALK, function () {
    builder.teleportTo(player.position())
    builder.place(CORNFLOWER)
})
player.onChat("plaatsBomen", function () {
    builder.teleportTo(world(2, 0, 5))
    builder.place(DARK_OAK_SAPLING)
    builder.move(FORWARD, 1)
    builder.place(ACACIA_SAPLING)
    builder.move(FORWARD, 1)
    builder.place(DARK_OAK_SAPLING)
    builder.move(FORWARD, 1)
    builder.place(ACACIA_SAPLING)
})
player.onChat("torenGoud", function () {
    builder.teleportTo(world(4, 0, 5))
    builder.place(GOLD_BLOCK)
    builder.move(UP, 1)
    builder.place(GOLD_BLOCK)
    builder.move(UP, 1)
    builder.place(GOLD_BLOCK)
})
player.onChat("afsluiting", function () {
    builder.teleportTo(world(-12, 0, 15))
    for (let index = 0; index < 4; index++) {
        for (let index = 0; index < 20; index++) {
            builder.place(SPRUCE_FENCE)
            builder.move(FORWARD, 1)
        }
        builder.turn(RIGHT_TURN)
    }
})

```

## Bomen

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je de bomen rij maakt.

[Klik hier om naar het leerplatform te gaan](https://leerplatform.codefever.be/).


## Goud toren

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je de goud toren.

[Klik hier om naar het leerplatform te gaan](https://leerplatform.codefever.be/).

## Bank

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je de bank maakt.

[Klik hier om naar het leerplatform te gaan](https://leerplatform.codefever.be/).

## Hoge toren

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je de hoge toren maakt.

[Klik hier om naar het leerplatform te gaan](https://leerplatform.codefever.be/).

## Afsluiting

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je de afsluiting maakt.

[Klik hier om naar het leerplatform te gaan](https://leerplatform.codefever.be/).

## Serre

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je de serre.

[Klik hier om naar het leerplatform te gaan](https://leerplatform.codefever.be/).
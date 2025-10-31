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

## Rups

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je een rups maakt.

[Klik hier om naar het leerplatform te gaan](https://leerplatform.codefever.be/).

![Rups](https://codefeverpublic.blob.core.windows.net/public-content/images/6d403f7a4b08ce078280874615075739ba056bf896fe900dfc5e858efbbb9bf1.png)

## Torentje van goud

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je een torentje van goud maakt.

![Torentje van goud](https://codefeverpublic.blob.core.windows.net/public-content/images/5e5342e535df76c288005ae0b0da79a57b7a3c7c076b56413110e10ea1f4650f.png)

## Trap

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je een trap maakt.

![Trap](https://codefeverpublic.blob.core.windows.net/public-content/images/88aa629f8d9778b632cec4cd53b7b5f6b8c5b22a87a9a8182824c05c53e50f72.png)

## Toren met lus

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je een trap maakt met behulp van lussen.

![Toren](https://codefeverpublic.blob.core.windows.net/public-content/images/0db2bf14c73e3eb8e69d96f03a554c3c340be45fb45d92ccaa16274283a4dbf8.png)

## Haak

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je een haak maakt.

![Haak](https://codefeverpublic.blob.core.windows.net/public-content/images/90e3a8a9754db98f546bea695b098b3721463ada131c13e5e2df9fbbacb6ff95.png)

## Vierkant

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je een vierkant maakt.

![Vierkant](https://codefeverpublic.blob.core.windows.net/public-content/images/19fa92227f6914d9a68a655415666f8756f49c02e772d4c136448a57380eff12.png)

## Glazen toren

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je een glazen toren maakt.

![Glazen toren](https://codefeverpublic.blob.core.windows.net/public-content/images/88c902207511d429dad83cc61929b311a4cb00be3fed7ef9cea9414e773109e6.png)

## Klein duimpje 2.0

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je klein duimpje 2.0 wordt.

![Klein duimpje 2.0](https://codefeverpublic.blob.core.windows.net/public-content/images/30f2d8a617a79288cb66e02a0b1d4b7065dccddc2ccb2f30b95bbffabc26f1b1.png)

## Extra opgaven

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor de extra opgaven.

![Extra opgaven](https://codefeverpublic.blob.core.windows.net/public-content/images/4d34ad7b95637fb1a65332c1d1f2227acce77f1a3b2a1fc5c570984f6ade763a.png)

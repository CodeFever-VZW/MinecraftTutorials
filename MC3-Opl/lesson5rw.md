# MC Reeks 3 Les 3

```template
let positie: Position = null

//level 1
player.onChat("level1", function () {
    positie = world(0, -57, 6)
    player.say(":)")
    for (let z = 0; z <= 9; z++) {
        if (!(blocks.testForBlock(EMERALD_BLOCK, positie))) {
            blocks.place(AIR, positie)
            player.say(positie)
        }
        positie = positions.add(
        positie,
        world(0, 0, 1)
        )
    }
})

//level 2
player.onChat("level2", function () {
    positie = world(-4, -57, 34)
    player.say(":)")
    for (let x = 0; x <= 8; x++) {
        for (let z = 0; z <= 8; z++) {
            if (!(blocks.testForBlock(EMERALD_BLOCK, positie))) {
                blocks.place(AIR, positie)
            }
            positie = positions.add(
            positie,
            world(0, 0, 1)
            )
        }
        positie = positions.add(
        positie,
        world(1, 0, -9)
        )
    }
})

//level 3
player.onChat("level3", function () {
    positie = world(-2, -57, 60)
    player.say(":)")
    for (let lengte = 0; lengte <= 2; lengte++) {
        for (let x = 0; x <= 4; x++) {
            for (let z = 0; z <= 4; z++) {
                if (!(blocks.testForBlock(EMERALD_BLOCK, positie))) {
                    blocks.place(AIR, positie)
                }
                positie = positions.add(
                positie,
                world(0, 0, 1)
                )
            }
            positie = positions.add(
            positie,
            world(1, 0, -5)
            )
        }
        positie = positions.add(
        positie,
        world(-5, 0, 8)
        )
    }
})

//level 4
player.onChat("level4", function () {
    positie = world(-10, -57, 99)
    player.say(":)")
    for (let breete = 0; breete <= 2; breete++) {
        for (let lengte = 0; lengte <= 2; lengte++) {
            for (let x = 0; x <= 4; x++) {
                for (let z = 0; z <= 4; z++) {
                    if (!(blocks.testForBlock(EMERALD_BLOCK, positie))) {
                        blocks.place(AIR, positie)
                    }
                    positie = positions.add(
                    positie,
                    world(0, 0, 1)
                    )
                }
                positie = positions.add(
                positie,
                world(1, 0, -5)
                )
            }
            positie = positions.add(
            positie,
            world(-5, 0, 8)
            )
        }
        positie = positions.add(
        positie,
        world(8, 0, -24)
        )
    }
})

// level 5
player.onChat("level5", function () {
    positie = world(-10, -57, 99)
    player.say(":)")
    for (let breete = 0; breete <= 2; breete++) {
        for (let lengte2 = 0; lengte2 <= 2; lengte2++) {
            for (let x3 = 0; x3 <= 4; x3++) {
                for (let z4 = 0; z4 <= 4; z4++) {
                    currentPos = positions.add(
                    positie,
                    world(x3 + breete * 8, 0, z4 + lengte2 * 8)
                    )
                    if (!(blocks.testForBlock(EMERALD_BLOCK, currentPos))) {
                        blocks.place(AIR, currentPos)
                    }
                }
            }
        }
    }
})


```

## Level 1

Zorg er voor dat je veilig over de drukplaten kan gaan door alle tnt er onder weg te halen.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

## Level 2

Zorg er voor dat je veilig over de drukplaten kan gaan door alle tnt er onder weg te halen.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

## Level 3

Zorg er voor dat je veilig over de drukplaten kan gaan door alle tnt er onder weg te halen.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

## Level 4

Zorg er voor dat je veilig over de drukplaten kan gaan door alle tnt er onder weg te halen.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

## Level 5

Zorg er voor dat je veilig over de drukplaten kan gaan door alle tnt er onder weg te halen.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.


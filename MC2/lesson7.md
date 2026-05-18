# Minecraft 2 les 7

```template
let lampionGeelStart: Position = null
let lampionGeelEinde: Position = null
let lampionRoodStart: Position = null
let lampionRoodEinde: Position = null
let lampionBlauwStart: Position = null
let lampionBlauwEinde: Position = null
let lampion = 0
function zetVariabelenKlaar () {
    lampionGeelStart = world(-15, 106, 0)
    lampionGeelEinde = world(-3, 115, 12)
    lampionRoodStart = world(-15, 106, 15)
    lampionRoodEinde = world(-3, 115, 27)
    lampionBlauwStart = world(-15, 106, 30)
    lampionBlauwEinde = world(-3, 115, 42)
}

player.onChat("lampionnen", function () {
    builder.teleportTo(world(0, 106, 0))
    builder.face(EAST)
    zetVariabelenKlaar()
})
```

```blocks
//setup variabelen
let lampionGeelStart: Position = null
let lampionGeelEinde: Position = null
let lampionRoodStart: Position = null
let lampionRoodEinde: Position = null
let lampionBlauwStart: Position = null
let lampionBlauwEinde: Position = null
let lampion = 0
function zetVariabelenKlaar () {
    lampionGeelStart = world(-15, 106, 0)
    lampionGeelEinde = world(-3, 115, 12)
    lampionRoodStart = world(-15, 106, 15)
    lampionRoodEinde = world(-3, 115, 27)
    lampionBlauwStart = world(-15, 106, 30)
    lampionBlauwEinde = world(-3, 115, 42)
}
//hoofd code, gaat per vakje een random lanteren zetten op een random hoogte
player.onChat("lampionnen", function () {
    builder.teleportTo(world(0, 106, 0))
    builder.face(EAST)
    zetVariabelenKlaar()
    for (let index = 0; index < 5; index++) {
        for (let index = 0; index < 5; index++) {
            lampion = randint(1, 5)
            if (lampion == 1) {
                blocks.clone(
                lampionGeelStart,
                lampionGeelEinde,
                positions.add(
                builder.position(),
                pos(0, randint(0, 25), 0)
                ),
                CloneMask.Replace,
                CloneMode.Force
                )
            } else if (lampion == 2) {
                blocks.clone(
                lampionRoodStart,
                lampionRoodEinde,
                positions.add(
                builder.position(),
                pos(0, randint(0, 25), 0)
                ),
                CloneMask.Replace,
                CloneMode.Force
                )
            } else if (lampion == 3) {
                blocks.clone(
                lampionBlauwStart,
                lampionBlauwEinde,
                positions.add(
                builder.position(),
                pos(0, randint(0, 25), 0)
                ),
                CloneMask.Replace,
                CloneMode.Force
                )
            } else {
                blocks.fill(
                AIR,
                builder.position(),
                positions.add(
                builder.position(),
                pos(13, 35, 13)
                ),
                FillOperation.Replace
                )
            }
            builder.move(FORWARD, 13)
        }
        builder.move(BACK, 13 * 5)
        builder.move(RIGHT, 13)
    }
})
//clear functie om bord terug leeg te maken
player.onChat("clear", function () {
    builder.teleportTo(world(0, 106, 0))
    builder.face(EAST)
    for (let index = 0; index < 5; index++) {
        for (let index = 0; index < 5; index++) {
            blocks.fill(
            AIR,
            builder.position(),
            positions.add(
            builder.position(),
            pos(13, 35, 13)
            ),
            FillOperation.Replace
            )
            builder.move(FORWARD, 13)
        }
        builder.move(BACK, 13 * 5)
        builder.move(RIGHT, 13)
    }
})

```

## Leerplatform

Gebruik het leerplatform om de oefening op te lossen.

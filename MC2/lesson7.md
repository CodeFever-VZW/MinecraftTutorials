# Minecraft 2 les 7

```template
let lantarenGeelStart: Position = null
let lantarenGeelEinde: Position = null
let lantarenRoodStart: Position = null
let lantarenRoodEinde: Position = null
let lantarenBlauwStart: Position = null
let lantarenBlauwEinde: Position = null
let lantaren = 0
function zetVariabelenKlaar () {
    lantarenGeelStart = world(-15, 106, 0)
    lantarenGeelEinde = world(-3, 115, 12)
    lantarenRoodStart = world(-15, 106, 15)
    lantarenRoodEinde = world(-3, 115, 27)
    lantarenBlauwStart = world(-15, 106, 30)
    lantarenBlauwEinde = world(-3, 115, 42)
}

player.onChat("lantarens", function () {
    builder.teleportTo(world(0, 106, 0))
    builder.face(EAST)
    zetVariabelenKlaar()
})
```

```blocks
//setup variabelen
let lantarenGeelStart: Position = null
let lantarenGeelEinde: Position = null
let lantarenRoodStart: Position = null
let lantarenRoodEinde: Position = null
let lantarenBlauwStart: Position = null
let lantarenBlauwEinde: Position = null
let lantaren = 0
function zetVariabelenKlaar () {
    lantarenGeelStart = world(-15, 106, 0)
    lantarenGeelEinde = world(-3, 115, 12)
    lantarenRoodStart = world(-15, 106, 15)
    lantarenRoodEinde = world(-3, 115, 27)
    lantarenBlauwStart = world(-15, 106, 30)
    lantarenBlauwEinde = world(-3, 115, 42)
}
//hoofd code, gaat per vakje een random lanteren zetten op een random hoogte
player.onChat("lantarens", function () {
    builder.teleportTo(world(0, 106, 0))
    builder.face(EAST)
    zetVariabelenKlaar()
    for (let index = 0; index < 5; index++) {
        for (let index = 0; index < 5; index++) {
            lantaren = randint(1, 5)
            if (lantaren == 1) {
                blocks.clone(
                lantarenGeelStart,
                lantarenGeelEinde,
                positions.add(
                builder.position(),
                pos(0, randint(0, 25), 0)
                ),
                CloneMask.Replace,
                CloneMode.Force
                )
            } else if (lantaren == 2) {
                blocks.clone(
                lantarenRoodStart,
                lantarenRoodEinde,
                positions.add(
                builder.position(),
                pos(0, randint(0, 25), 0)
                ),
                CloneMask.Replace,
                CloneMode.Force
                )
            } else if (lantaren == 3) {
                blocks.clone(
                lantarenBlauwStart,
                lantarenBlauwEinde,
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
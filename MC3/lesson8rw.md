# MC Reeks 3 Les 8
```template


function bouwIngang () {
}


function bouwSchacht (hoogte: number) {
}

function bouwUitgang (beginHoogte: number) {
}


player.onChat("blok", function () {
    blocks.fill(
    GRASS,
    pos(-5, 3, -5),
    pos(5, randint(10, 20), 5),
    FillOperation.Replace
    )
})

```




```block


  function bouwIngang () {
    blocks.fill(
    GLASS,
    pos(-1, -1, 1),
    pos(1, 2, 3),
    FillOperation.Replace
    )
    blocks.place(SOUL_SAND, pos(0, -1, 2))
    blocks.fill(
    OAK_SIGN,
    pos(0, 0, 1),
    pos(0, 1, 1),
    FillOperation.Replace
    )
    blocks.fill(
    WATER,
    pos(0, 0, 2),
    pos(0, 2, 2),
    FillOperation.Replace
    )
}


player.onChat("uitgang", function () {
    bouwUitgang(2)
})

player.onChat("outside", function () {
    player.teleport(pos(0, 70, 0))

})




function bouwSchacht (hoogte: number) {
    player.say("bouwschacht")
    blocks.fill(
    GLASS,
    pos(-1, hoogte, 1),
    pos(1, hoogte, 3),
    FillOperation.Replace
    )
    blocks.place(WATER, pos(0, hoogte, 2))
}


player.onChat("lift", function () {
    bouwIngang()
    Y = 3
    while (!(blocks.testForBlock(AIR, pos(0, Y, 2)))) {
        bouwSchacht(Y)
        Y += 1
    }
    player.say("klaar")
})

player.onChat("liftDown", function () {
    Y = -1
    while (!(blocks.testForBlock(AIR, pos(0, Y, 2)))) {
        bouwSchacht(Y)
        Y += -1
    }
    bouwUitgang(Y)
    player.say("klaar")
})

player.onChat("lift20", function () {
    bouwIngang()
    for (let index = 0; index <= 19; index++) {
        bouwSchacht(3 + index)
    }
    player.say("klaar")
})

function bouwUitgang (beginHoogte: number) {
    blocks.fill(
    GLASS,
    pos(-1, beginHoogte, 1),
    pos(1, beginHoogte - 2, 3),
    FillOperation.Replace
    )
    blocks.place(MAGMA_BLOCK, pos(0, beginHoogte - 2, 2))
    blocks.fill(
    OAK_SIGN,
    pos(0, 0, 1),
    pos(0, beginHoogte - 1, 1),
    FillOperation.Replace
    )
    blocks.fill(
    WATER,
    pos(0, beginHoogte, 2),
    pos(0, beginHoogte - 1, 2),
    FillOperation.Replace
    )
}

player.onChat("help", function () {
    player.teleport(world(68, 63, -130))
})

player.onChat("ingang", function () {
    bouwIngang()
})

player.onChat("blok", function () {
    blocks.fill(
    GRASS,
    pos(-5, 3, -5),
    pos(5, randint(10, 20), 5),
    FillOperation.Replace
    )
})

player.onChat("gaKamer", function (num1) {
    player.teleport(lijstKamers[num1])
})

let Y = 0
let lijstKamers: Position[] = []
gameplay.setGameMode(
CREATIVE,
mobs.target(LOCAL_PLAYER)
)
lijstKamers = [
world(-2, 64, -146),
world(-8, 74, -145),
world(-19, 89, -145),
world(-17, 101, -177),
world(-6, 86, -141),
world(-56, 106, -141),
world(-58, 81, -142),
world(-58, 64, -209),
world(-97, 82, -240),
world(-97, 93, -240)
]
```
## Maak een lift
Maak een lift omhoog
Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

## Maak een lift omlaag
Maak een lift omlaag
Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

## Ga naar de echte wereld
Download nu de echt opdrachtwereld en ontsnap uit de berg
Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

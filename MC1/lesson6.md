# MC Reeks 1 Les 5

```template
player.onChat("goudkoorts", function () {})
```

```block
let aantalGoudBlokken = 0
let aantalPaarseBlokken = 0
let aantalSeconden = 0
let aantalMagmaBlokken = 0
let xMagma = 0
let yMagma = 0
let zMagma = 0
let xGoud = 0
let yGoud = 0
let zGoud = 0
blocks.onBlockBroken(GOLD_BLOCK, function () {
    aantalGoudBlokken += -1
    player.say("Goud blok gevonden! Nog " + aantalGoudBlokken + "goudblokken te vinden.")
})
player.onChat("goudkoorts", function () {
    blocks.fill(
    PURPLE_WOOL,
    pos(-5, -1, -5),
    pos(2, -3, 2),
    FillOperation.Replace
    )
    aantalPaarseBlokken = 0
    aantalSeconden = 0
    aantalGoudBlokken = 3
    aantalMagmaBlokken = 8
    for (let index = 0; index < aantalGoudBlokken; index++) {
        zetGoudBlokken()
    }
    for (let index = 0; index < aantalMagmaBlokken; index++) {
        zetMagmaBlokken()
    }
    while (aantalGoudBlokken > 0 || aantalMagmaBlokken < 8) {
        loops.pause(1000)
        aantalSeconden += 1
    }
    if (aantalGoudBlokken > 0) {
        player.say("Ik heb ze allemaal gevonden na " + aantalSeconden + " seconden na " + aantalPaarseBlokken + "paarse blokken kapot te slaan!")
    } else if (aantalMagmaBlokken < 8) {
        player.say("GAME OVER! Je raakte een magmablok!")
    }
})
blocks.onBlockBroken(MAGMA_BLOCK, function () {
    aantalMagmaBlokken += -1
})
blocks.onBlockBroken(PURPLE_WOOL, function () {
    aantalPaarseBlokken += 1
})
function zetMagmaBlokken () {
    xMagma = randint(-5, 5)
    yMagma = randint(-3, -2)
    zMagma = randint(-5, 5)
    if (blocks.testForBlock(GOLD_BLOCK, pos(xMagma, yMagma, zMagma))) {
        zetMagmaBlokken()
    } else if (blocks.testForBlock(MAGMA_BLOCK, pos(xMagma, yMagma, zMagma))) {
        zetMagmaBlokken()
    } else {
        blocks.place(MAGMA_BLOCK, pos(xMagma, yMagma, zMagma))
    }
}
function zetGoudBlokken () {
    xGoud = randint(-5, 5)
    yGoud = randint(-3, -2)
    zGoud = randint(-5, 5)
    if (blocks.testForBlock(GOLD_BLOCK, pos(xGoud, yGoud, zGoud))) {
        zetGoudBlokken()
    } else if (blocks.testForBlock(MAGMA_BLOCK, pos(xGoud, yGoud, zGoud))) {
        zetGoudBlokken()
    } else {
        blocks.place(GOLD_BLOCK, pos(xGoud, yGoud, zGoud))
    }
}

```

## Goudkoorts

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je de opdracht maakt.

[Klik hier om naar het leerplatform te gaan](https://leerplatform.codefever.be/).
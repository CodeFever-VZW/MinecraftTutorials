# MC Reeks 3 Les 4

```template
let gewonnen = 0
let startX = 0
let startY = 0
let startZ = 0
blocks.onBlockPlaced(RED_WOOL, function () {
    player.say("rood")
    if (gewonnen == 0) {
        checkVeld()
        if (gewonnen >= 1) {
            player.say("De rode speler heeft gewonnen!")
        }
    }
})
function checkDiagonaal2 () {
    if (blocks.testForBlock(RED_WOOL, world(startX + 0, startY, startZ + 2))) {
        if (blocks.testForBlock(BLUE_WOOL, world(startX + 1, startY, startZ + 1))) {
            if (blocks.testForBlock(RED_WOOL, world(startX + 2, startY, startZ + 0))) {
                gewonnen = 1
            }
        }
    }
    if (blocks.testForBlock(BLUE_WOOL, world(startX + 0, startY, startZ + 2))) {
        if (blocks.testForBlock(RED_WOOL, world(startX + 1, startY, startZ + 1))) {
            if (blocks.testForBlock(BLUE_WOOL, world(startX + 2, startY, startZ + 0))) {
                gewonnen = 1
            }
        }
    }
}
function checkZAs (x: number, y: number, z: number) {
    if (blocks.testForBlock(RED_WOOL, world(x, y, z + 0))) {
        if (blocks.testForBlock(BLUE_WOOL, world(x, y, z + 1))) {
            if (blocks.testForBlock(RED_WOOL, world(x, y, z + 2))) {
                gewonnen = 1
            }
        }
    }
    if (blocks.testForBlock(BLUE_WOOL, world(x, y, z + 0))) {
        if (blocks.testForBlock(RED_WOOL, world(x, y, z + 1))) {
            if (blocks.testForBlock(BLUE_WOOL, world(x, y, z + 2))) {
                gewonnen = 1
            }
        }
    }
}
player.onChat("oxo", function () {
    gewonnen = 0
    startX = 69
    startY = 71
    startZ = 14
    blocks.fill(
    STONE_BRICKS,
    world(68, 70, 13),
    world(72, 71, 17),
    FillOperation.Replace
    )
    blocks.fill(
    AIR,
    world(69, 71, 14),
    world(71, 71, 16),
    FillOperation.Replace
    )
})
function checkDiagonaal1 () {
    if (blocks.testForBlock(RED_WOOL, world(startX + 0, startY, startZ + 0))) {
        if (blocks.testForBlock(BLUE_WOOL, world(startX + 1, startY, startZ + 1))) {
            if (blocks.testForBlock(RED_WOOL, world(startX + 2, startY, startZ + 2))) {
                gewonnen = 1
            }
        }
    }
    if (blocks.testForBlock(BLUE_WOOL, world(startX + 0, startY, startZ + 0))) {
        if (blocks.testForBlock(RED_WOOL, world(startX + 1, startY, startZ + 1))) {
            if (blocks.testForBlock(BLUE_WOOL, world(startX + 2, startY, startZ + 2))) {
                gewonnen = 1
            }
        }
    }
}
function checkVeld () {
    for (let index = 0; index <= 2; index++) {
        checkXAs(startX, startY, startZ + index)
        checkZAs(startX + index, startY, startZ)
    }
    checkDiagonaal1()
    checkDiagonaal2()
}
blocks.onBlockPlaced(BLUE_WOOL, function () {
    player.say("blauw")
    if (gewonnen == 0) {
        checkVeld()
        if (gewonnen >= 1) {
            player.say("De blauwe speler heeft gewonnen!")
        }
    }
})
function checkXAs (x: number, y: number, z: number) {
    if (blocks.testForBlock(RED_WOOL, world(x + 0, y, z))) {
        if (blocks.testForBlock(BLUE_WOOL, world(x + 1, y, z))) {
            if (blocks.testForBlock(RED_WOOL, world(x + 2, y, z))) {
                gewonnen = 1
            }
        }
    }
    if (blocks.testForBlock(BLUE_WOOL, world(x + 0, y, z))) {
        if (blocks.testForBlock(RED_WOOL, world(x + 1, y, z))) {
            if (blocks.testForBlock(BLUE_WOOL, world(x + 2, y, z))) {
                gewonnen = 1
            }
        }
    }
}
```

## OXO

We gaan het spel OXO maken!

Alle uitleg die je nodig hebt kan je vinden op het [leerplatform](https://leerplatform.codefever.be/).

## Extra: Gouden win!

Pas je code aan zodanig dat de blokken die de winnende OXO vormen goud blokken worden.

voorbeeld: (-- insert foto here --)

## Extra: Extra Speler

!! Deze extra opdracht is niet makkelijk en is een echt uitdaging voor zij die het graag extra moeilijk hebben !!

Pas je code aan zodat je met een extra speler kan spelen. BV geel.
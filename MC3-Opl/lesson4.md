# MC Reeks 3 Les 4

```template
let startX = 0
let startY = 0
let startZ = 0
function tribune3_2 () {
    for (let index = 0; index <= 10; index++) {
        blocks.fill(
        GRANITE,
        world(startX - 15, startY + index, 0 - 5 - index),
        world(startX + 45, startY + index, startZ - 15),
        FillOperation.Replace
        )
    }
}
function publiek () {
    for (let index = 0; index <= 50; index++) {
        mobs.spawn(VILLAGER, randpos(
        world(startX - 15, startY + 10, startZ - 15),
        world(startX + 45, startY + 10, startZ + 45)
        ))
    }
}
function tribune2_2 () {
    for (let index = 0; index <= 10; index++) {
        blocks.fill(
        GRANITE,
        world(startX + 35 + index, startY + index, startZ + 45),
        world(startX + 45, startY + index, startZ - 15),
        FillOperation.Replace
        )
    }
}
function tribune3 () {
    for (let index = 0; index <= 10; index++) {
        blocks.fill(
        GRANITE,
        world(startX - 5, startY + index, 0 - 5 - index),
        world(startX + 35, startY + index, startZ - 15),
        FillOperation.Replace
        )
    }
}
function tribune4 () {
    for (let index = 0; index <= 10; index++) {
        blocks.fill(
        GRANITE,
        world(startX + 35, startY + index, startZ + 35 + index),
        world(startX - 5, startY + index, startZ + 45),
        FillOperation.Replace
        )
    }
}
function tribune1_2 () {
    for (let index = 0; index <= 10; index++) {
        blocks.fill(
        GRANITE,
        world(startX - 5 - index, startY + index, startZ - 15),
        world(startX - 15, startY + index, startZ + 45),
        FillOperation.Replace
        )
    }
}
function tribune2 () {
    for (let index = 0; index <= 10; index++) {
        blocks.fill(
        GRANITE,
        world(startX + 35 + index, startY + index, startZ + 35),
        world(startX + 45, startY + index, startZ - 5),
        FillOperation.Replace
        )
    }
}
function uitgang () {
    blocks.fill(
    AIR,
    world(startX - 5, startY, startZ + 14),
    world(startX - 15, startY + 2, startZ + 16),
    FillOperation.Replace
    )
}
player.onChat("arena2", function () {
    zetKlaar()
    tribune1_2()
    tribune2_2()
    tribune3_2()
    tribune4_2()
    uitgang()
    publiek()
    player.say("Klaar met bouwen!")
})
function tribune4_2 () {
    for (let index = 0; index <= 10; index++) {
        blocks.fill(
        GRANITE,
        world(startX + 45, startY + index, startZ + 35 + index),
        world(startX - 15, startY + index, startZ + 45),
        FillOperation.Replace
        )
    }
}
function tribune1 () {
    for (let index = 0; index <= 10; index++) {
        blocks.fill(
        GRANITE,
        world(startX - 5 - index, startY + index, startZ - 5),
        world(startX - 15, startY + index, startZ + 35),
        FillOperation.Replace
        )
    }
}
function zetKlaar () {
    startX = 55
    startY = 70
    startZ = 0
    mobs.kill(
    mobs.target(ALL_ENTITIES)
    )
    gameplay.setWeather(CLEAR)
}
player.onChat("arena", function () {
    zetKlaar()
    tribune1()
    tribune2()
    tribune3()
    tribune4()
})

```

## Speelveld

Gebruik zeker de startcoördinaten!

Als er iets mis gaat kan je het reset item gebruiken om opnieuw te proberen.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Snakepit](https://codefeverpublic.blob.core.windows.net/public-content/images/b2d975509d6804759ee55656470bbdd16f4a313ad6b20be26e859ebd6b2a020b.png)

## Tribune

Begin bij tribune 1.
Gebruik de functies en vul je code hier in.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Tribune](https://codefeverpublic.blob.core.windows.net/public-content/images/e4218de35048b39365a820be94ffafa268915ab84f065b7e70681a0084422692.png)

## Meerdere tribunes

Werk verder aan Tribunes 2, 3 en 4.
Gebruik de functies en pas je code aan voor de nieuwe tribunes.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Meerdere tribunes](https://codefeverpublic.blob.core.windows.net/public-content/images/9d70747c652666f1aa0673c510fee15b9d0d2bfbda0507da9b6937b4582e72d2.png)

## Gesloten arena

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Gesloten arena](https://codefeverpublic.blob.core.windows.net/public-content/images/2f009506689aa1024161faa11549e82c3b81ffc1c2c5d0d770a15e74260ed62e.png)

## Uitgang (Extra)

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Uitgang](https://codefeverpublic.blob.core.windows.net/public-content/images/662d69c23abe031d6e089378da7c45ace73c03e8fea5ee2658b930d50f1bfcfb.png)

# MC Reeks 3 Les 4

```template
let startX = 0
let startY = 0
let startZ = 0
function tribune3 () {
    for (let index = 0; index <= 10; index++) {
        blocks.fill(
        POLISHED_GRANITE,
        world(startX + -5, startY + index, startZ + (35 + index)),
        world(startX + 35, startY + index, startZ + 45),
        FillOperation.Replace
        )
    }
}
function tribune4 () {
    for (let index2 = 0; index2 <= 10; index2++) {
        blocks.fill(
        POLISHED_GRANITE,
        world(startX + -5, startY + index2, startZ - (5 + index2)),
        world(startX + 35, startY + index2, startZ - 15),
        FillOperation.Replace
        )
    }
}
function hoek1 () {
    blocks.fill(
    POLISHED_GRANITE,
    world(startX - 5, startY + 0, startZ - 5),
    world(startX - 15, startY + 10, startZ - 15),
    FillOperation.Replace
    )
    for (let index4 = 0; index4 <= 10; index4++) {
        blocks.fill(
        AIR,
        world(startX - 5, startY + (11 - index4), startZ - 5),
        world(startX - (15 - index4), startY + (11 - index4), startZ - (15 - index4)),
        FillOperation.Replace
        )
    }
}
function tribune2 () {
    for (let index3 = 0; index3 <= 10; index3++) {
        blocks.fill(
        POLISHED_GRANITE,
        world(startX + (35 + index3), startY + index3, startZ - 5),
        world(startX + 45, startY + index3, startZ + 35),
        FillOperation.Replace
        )
    }
}
function hoek2 () {
    blocks.fill(
    POLISHED_GRANITE,
    world(startX - 5, startY + 0, startZ + 35),
    world(startX - 15, startY + 10, startZ + 45),
    FillOperation.Replace
    )
    for (let index4 = 0; index4 <= 10; index4++) {
        blocks.fill(
        AIR,
        world(startX - 5, startY + (11 - index4), startZ + 35),
        world(startX - (15 - index4), startY + (11 - index4), startZ + (45 - index4)),
        FillOperation.Replace
        )
    }
}
player.onChat("tribune", function () {
    zetVariabelenKlaar()
    speelveld()
    tribune1()
    tribune2()
    tribune3()
    tribune4()
    hoek1()
    hoek2()
    hoek3()
    hoek4()
    ingang()
    player.say("Klaar met bouwen!")
})
function hoek4 () {
    blocks.fill(
    POLISHED_GRANITE,
    world(startX + 35, startY + 0, startZ - 5),
    world(startX + 45, startY + 10, startZ - 15),
    FillOperation.Replace
    )
    for (let index4 = 0; index4 <= 10; index4++) {
        blocks.fill(
        AIR,
        world(startX + 35, startY + (11 - index4), startZ - 5),
        world(startX + (45 - index4), startY + (11 - index4), startZ - (15 - index4)),
        FillOperation.Replace
        )
    }
}
function ingang () {
    blocks.fill(
    AIR,
    world(startX + -5, startY + 0, startZ + 14),
    world(startX + -15, startY + 2, startZ + 16),
    FillOperation.Replace
    )
}
function speelveld () {
    blocks.fill(
    COBBLESTONE,
    world(startX + 0, startY + 0, startZ + 0),
    world(startX + 30, startY + 1, startZ + 30),
    FillOperation.Replace
    )
    blocks.fill(
    AIR,
    world(startX + 1, startY + 1, startZ + 1),
    world(startX + 29, startY + 1, startZ + 29),
    FillOperation.Replace
    )
}
function zetVariabelenKlaar () {
    startX = 55
    startY = 70
    startZ = 0
}
function tribune1 () {
    for (let index4 = 0; index4 <= 10; index4++) {
        blocks.fill(
        POLISHED_GRANITE,
        world(startX - (5 + index4), startY + index4, startZ - 5),
        world(startX - 15, startY + index4, startZ + 35),
        FillOperation.Replace
        )
    }
}
function hoek3 () {
    blocks.fill(
    POLISHED_GRANITE,
    world(startX + 35, startY + 0, startZ + 35),
    world(startX + 45, startY + 10, startZ + 45),
    FillOperation.Replace
    )
    for (let index4 = 0; index4 <= 10; index4++) {
        blocks.fill(
        AIR,
        world(startX + 35, startY + (11 - index4), startZ + 35),
        world(startX + (45 - index4), startY + (11 - index4), startZ + (45 - index4)),
        FillOperation.Replace
        )
    }
}

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

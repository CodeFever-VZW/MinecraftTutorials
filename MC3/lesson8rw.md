```package
minecraft
```

# MC Reeks 3 - Les 8: Lift Bouwen

In deze les ga je een lift maken in Minecraft met code. 🚀

---

## Stap 1: Ingang bouwen

We beginnen met het maken van de ingang van de lift.

```blocks
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
```

---

## Stap 2: Schacht bouwen

We maken een functie die een stuk van de liftbuis bouwt.

```blocks
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
```

---

## Stap 3: Uitgang bouwen

Bovenaan je lift komt een uitgang met een magma blok om je naar beneden te trekken.

```blocks
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
```

---

## Stap 4: Automatische lift omhoog

We gaan nu een automatische lift omhoog maken tot aan het eerste luchtblok.

```blocks
let Y = 0
player.onChat("lift", function () {
    bouwIngang()
    Y = 3
    while (!(blocks.testForBlock(AIR, pos(0, Y, 2)))) {
        bouwSchacht(Y)
        Y += 1
    }
    player.say("klaar")
})
```

---

## Stap 5: Automatische lift omlaag

Deze versie zoekt naar beneden tot hij lucht vindt en bouwt dan de uitgang.

```blocks
player.onChat("liftDown", function () {
    Y = -1
    while (!(blocks.testForBlock(AIR, pos(0, Y, 2)))) {
        bouwSchacht(Y)
        Y += -1
    }
    bouwUitgang(Y)
    player.say("klaar")
})
```

---

## Stap 6: Handmatig 20 blokken omhoog

Maak een vaste lift van 20 blokken hoog.

```blocks
player.onChat("lift20", function () {
    bouwIngang()
    for (let index = 0; index <= 19; index++) {
        bouwSchacht(3 + index)
    }
    player.say("klaar")
})
```

---

## Stap 7: Extra functies

Een paar extra's om te testen.

```blocks
player.onChat("ingang", function () {
    bouwIngang()
})

player.onChat("uitgang", function () {
    bouwUitgang(2)
})

player.onChat("outside", function () {
    player.teleport(pos(0, 70, 0))
})

player.onChat("blok", function () {
    blocks.fill(
        GRASS,
        pos(-5, 3, -5),
        pos(5, randint(10, 20), 5),
        FillOperation.Replace
    )
})
```

---

## Stap 8: Kamersysteem

Teleporteren naar kamers met een lijst.

```blocks
let lijstKamers: Position[] = []
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

player.onChat("gaKamer", function (num1) {
    player.teleport(lijstKamers[num1])
})

gameplay.setGameMode(CREATIVE, mobs.target(LOCAL_PLAYER))
```

---

## Stap 9: Helpknop

Teleporteer naar de hulpzone.

```blocks
player.onChat("help", function () {
    player.teleport(world(68, 63, -130))
})
```

---

## Je lift is klaar!

Je hebt nu een functionele lift gebouwd met een ingang, schacht en uitgang. Probeer ook de extra functies uit!

Ga naar het [leerplatform](https://leerplatform.codefever.be/) voor meer opdrachten en uitleg.

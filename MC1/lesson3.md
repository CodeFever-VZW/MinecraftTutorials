# MC Reeks 1 Les 3

```template
player.onChat("spawn", function () {})
player.onChat("kippenregen", function () {})
```

```block
player.onChat("", function () {
    for (let index = 0; index < 4; index++) {
        mobs.spawn(CHICKEN, pos(randint(0, 10), 0, 0))
    }
    blocks.place(GRASS, world(0, 0, 0))
    blocks.fill(
    GRASS,
    pos(0, 0, 0),
    pos(0, 0, 0),
    FillOperation.Replace
    )
})
```

## Spawnen

Kijk op het leerplatform hoe je dieren en monsters spawnt.

![Spawnen](https://codefeverpublic.blob.core.windows.net/public-content/images/71957348b7d7626169e457f3ee303ef225e65256eb503a227c1212faa4a989b0.png)

## Kippenregen

Kijk op het leerplatform hoe je het kippen laat regenen.

![Kippenregen](https://codefeverpublic.blob.core.windows.net/public-content/images/87809b863eacf103b6be12fd7ed4112f97338240c952cdf43a4a3be5f0df29cb.png)

## Snelbouw

Kijk op het leerplatform hoe je snel gebouwen kan plaatsen.

![Snelbouw](https://codefeverpublic.blob.core.windows.net/public-content/images/9b446bbe1fc5eb802d5834534f99cd65c25cc7820da0479ad39277425d91f904.png)

## Bouwen door te vernietigen

Kijk op het leerplatform hoe je kan bouwen door te vernietigen.

![Bouwen door te vernietigen](https://codefeverpublic.blob.core.windows.net/public-content/images/0faa68d194645bc65172f6ee4c4dd3329c077b5797eece2019891cc63881a435.png)

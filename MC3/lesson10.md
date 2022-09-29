# MC Reeks 3 Les 10

```template
player.onChat("bombardeer", function () {})
```

```block
let x = 0
player.onChat("jump", function () {
    for (let index = 0; index < 4; index++) {
        x = randint(0, 10)
    }
    blocks.place(GRASS, world(x, 0, 0))
    loops.pause(100)
})
player.onTravelled(WALK, function () {
    blocks.replace(
    GRASS,
    GRASS,
    pos(0, 0, 0),
    pos(0, 0, 0)
    )
})


```

## Bombardeer
Vind de verborgen tempel door de berg weg te blazen.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Bombardeer](https://codefeverpublic.blob.core.windows.net/public-content/images/1f3a19dfd21ec52e26b748d867b1f2f58a17db50afc65afe2296f6c0c6ab337b.png)
    

## Licht aandoen
Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Licht aandoen](https://codefeverpublic.blob.core.windows.net/public-content/images/28d96ccf81de56ec83be8d7fb9fde38257b08141f836f19aac9b005e0dd6becd.png)
# MC Reeks 1 Les 4

```template
player.onChat("lava", function () {})
player.onChat("douche", function () {})
```

```block
player.onChat("", function () {
    while (!(blocks.testForBlock(GRASS, pos(0, 0, 0)))) {
        if (blocks.testForBlock(GRASS, pos(0, 0, 0)) || player.position().getValue(Axis.X) == 0) {
            blocks.fill(
            GRASS,
            pos(0, 0, 0),
            pos(0, 0, 0),
            FillOperation.Replace
            )
        }
    }
    builder.teleportTo(world(0, 0, 0))
    builder.place(GRASS)
    builder.move(FORWARD, 1)
    for (let index = 0; index < 4; index++) {
    	
    }
    blocks.place(GRASS, pos(0, 0, 0))
    mobs.spawn(CHICKEN, pos(randint(0, 10), 0, 0))
})
```

## The floor is lava

Kijk op het leerplatform hoe van de vloer lava maakt.

![The floor is lava](https://codefeverpublic.blob.core.windows.net/public-content/images/b2d985346f98d21e17bce8a52b49b89382e2ff3dc5de661b69f453defd35601e.png)

## Douche

Kijk op het leerplatform hoe je een douche maakt.

![Douche](https://codefeverpublic.blob.core.windows.net/public-content/images/8f111f353a563910041270e0b32d9bd23aafddccbbd56a70759f6270aeab30ed.png)

## Spookhuis

Kijk op het leerplatform hoe je een spookhuis maakt.

![Spookhuis](https://media.giphy.com/media/Yph6D7zPIVtIc/giphy.gif)

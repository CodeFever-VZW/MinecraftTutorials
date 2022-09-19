# MC Reeks 3 Les 3

```template
player.onChat("level1", function () {})
player.onChat("level2", function () {})
```

```block
player.onChat("run", function () {
    builder.move(FORWARD, 1)
    builder.turn(LEFT_TURN)
    builder.mark()
    builder.teleportTo(builder.position())
    builder.teleportTo(world(0, 0, 0))
    builder.place(GRASS)
    builder.tracePath(GRASS)
    builder.shift(1, 1, 1)
    builder.fill(GRASS)
    builder.line(GRASS)
    builder.face(WEST)
    builder.setOrigin()
    builder.teleportToOrigin()
    builder.raiseWall(GRASS, 5)
    builder.copy()
    builder.paste()
    builder.pushState()
    builder.popState()
    if (blocks.testForBlock(GRASS, pos(0, 0, 0))) {
    }
    for (let index = 0; index < 4; index++) {
        player.say(":)")
    }
})
```

## Level 1

Programmeer de bouwer om de 5 goudblokken te vinden.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Level 1](https://codefeverpublic.blob.core.windows.net/public-content/images/d8f2f1d0aa1cb23583ac9bae42084e903b7bcc2e059774f9ca52129147fb13f4.png)

## Level 2

Programmeer de bouwer om de 20 goudblokken te vinden.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

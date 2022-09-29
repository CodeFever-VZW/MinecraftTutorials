# MC Reeks 3 Les 5

```template
let startZ = 0
let startY = 0
let startX = 0
startX = 270
startY = 68
startZ = 46
gameplay.timeSet(gameplay.time(DAY))
gameplay.setWeather(CLEAR)
player.onChat("ontmijn", function () {})
```

```block
player.onChat("jump", function () {
    for (let index = 0; index <= 4; index++) {

    }
    builder.move(FORWARD, 1)
    builder.turn(LEFT_TURN)
    builder.mark()
    builder.teleportTo(world(0, 0, 0))
    builder.place(GRASS)
    builder.tracePath(GRASS)
    builder.shift(1, 1, 0 + 0)
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
    if (blocks.testForBlock(GRASS, builder.position())) {

    }
    player.say(":)")
    index += 1
})
let index = 0
let startX = 270
let startY = 68
let startZ = 46
gameplay.timeSet(gameplay.time(DAY))
gameplay.setWeather(CLEAR)
```

## Minefield

Jullie moeten dit mijnenveld onschadelijk maken. Gebruik zeker de startcoördinaten!

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Minefield](https://codefeverpublic.blob.core.windows.net/public-content/images/81134b44bf2caadde997349b385042eb191521019688b95423b94d9229ec211d.png)

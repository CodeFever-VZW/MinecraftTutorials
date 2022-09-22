# MC Reeks 3 Les 6

```template
player.onChat("graaf", function () {})
```

```block
let list: number[] = []
let text_list: number[] = []
player.onChat("run", function () {
    list = [list[0], 1]
    text_list = [
    [],
    list.length,
    list.removeAt(0),
    [list.pop(), list.shift(), list._pickRandom()]
    ]
    list[0] = list.unshift(GRASS)
    list.push(player.name())
    list.pop()
    list.shift()
    list.unshift(agent.getPosition())
    list.insertAt(CHICKEN, list.indexOf(IRON_SHOVEL))
    list.removeAt(mobs.monster(ZOMBIE))
    list.reverse()
    blocks.replace(
    GRASS,
    GRASS,
    world(0, 0, 0),
    pos(0, 0, 0)
    )
    for (let index = 0; index <= 4; index++) {

    }
    if (blocks.testForBlock(GRASS, pos(0 + 0, 0, 0))) {

    }
    blocks.place(GRASS, pos(0, 0, 0))
})

```

## Hoop zand vrijmaken

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Hoop zand](https://codefeverpublic.blob.core.windows.net/public-content/images/b1683247f963088b490af4ea7e617f76256c09872d26f4a39783a8d005ea88ea.png)

## Toegang tot schattenkamer vrijmaken

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Schatkamer](https://codefeverpublic.blob.core.windows.net/public-content/images/f30a00e5d4a01520910652b01d9aa4fd5a60c456389853a77d025c387842416b.png)

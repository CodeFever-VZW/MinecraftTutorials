# MC Reeks 1 Les 9

```template
player.onChat("spleef", function () {});
player.onChat("tntrun", function () {});
player.onChat("shootout", function () {});

// deze code moet je niet aan komen!
function startTntRun () {
    player.execute(
    "clear @a"
    )
    player.execute(
    "gamerule tntexplodes false"
    )
    player.say("§aTnt run start binnen 5 seconden!")
    loops.pause(2000)
    player.say("§a3 seconden!")
    loops.pause(1000)
    player.say("§a2 seconden!")
    loops.pause(1000)
    player.say("§a1 second!")
    loops.pause(1000)
    player.say("§aStart!")
    player.execute(
    "gamerule tntexplodes true"
    )
}

// deze code moet je niet aan komen!
function startShootOut () {
    player.execute(
    "/scriptevent codefever:start-shoot-out " + "{" + ("\"x\":" + player.position().getValue(Axis.X) + ",") + ("\"y\":" + player.position().getValue(Axis.Y) + ",") + ("\"z\":" + player.position().getValue(Axis.Z)) + "}"
    )
    player.execute(
    "gamerule pvp false"
    )
    player.say("§aShootout start binnen 5 seconden!")
    loops.pause(2000)
    player.say("§a3 seconden!")
    loops.pause(1000)
    player.say("§a2 seconden!")
    loops.pause(1000)
    player.say("§a1 second!")
    loops.pause(1000)
    player.say("§aStart!")
    player.execute(
    "gamerule pvp true"
    )
}
```

```block
let hoogte = 0
// deze code zorgt er voor de dat tnt niet aan gaat in het begin, en dan na 5 seconden wel
function startTntRun () {
    player.execute(
    "clear @a"
    )
    player.execute(
    "gamerule tntexplodes false"
    )
    player.say("§aTnt run start binnen 5 seconden!")
    loops.pause(2000)
    player.say("§a3 seconden!")
    loops.pause(1000)
    player.say("§a2 seconden!")
    loops.pause(1000)
    player.say("§a1 second!")
    loops.pause(1000)
    player.say("§aStart!")
    player.execute(
    "gamerule tntexplodes true"
    )
}
//maak de spleef arena
player.onChat("spleef", function () {
    hoogte = 0
    for (let index = 0; index < 10; index++) {
        shapes.circle(
        LIGHT_GRAY_CONCRETE,
        pos(0, hoogte, 0),
        21,
        Axis.Y,
        ShapeOperation.Outline
        )
        hoogte += 1
    }
    shapes.circle(
    SNOW,
    pos(0, 6, 0),
    21,
    Axis.Y,
    ShapeOperation.Replace
    )
    player.teleport(pos(0, 7, 0))
    mobs.give(
    mobs.target(ALL_PLAYERS),
    IRON_SHOVEL,
    1
    )
})
//maak de tnt run arena
player.onChat("tntrun", function () {
    hoogte = 0
    shapes.circle(
    TNT,
    pos(0, 6, 0),
    20,
    Axis.Y,
    ShapeOperation.Replace
    )
    shapes.circle(
    SAND,
    pos(0, 7, 0),
    20,
    Axis.Y,
    ShapeOperation.Replace
    )
    shapes.circle(
    STONE_PRESSURE_PLATE,
    pos(0, 8, 0),
    20,
    Axis.Y,
    ShapeOperation.Replace
    )
    for (let index = 0; index < 12; index++) {
        shapes.circle(
        LIGHT_GRAY_CONCRETE,
        pos(0, hoogte, 0),
        20,
        Axis.Y,
        ShapeOperation.Outline
        )
        hoogte += 1
    }
    player.teleport(pos(0, 10, 0))
    startTntRun()
})
//maak de schoot out arena
player.onChat("shootout", function () {
    blocks.fill(
    LIGHT_GRAY_CONCRETE,
    pos(3, 0, 10),
    pos(7, 10, -10),
    FillOperation.Replace
    )
    blocks.fill(
    LIGHT_GRAY_CONCRETE,
    pos(-3, 0, 10),
    pos(-7, 10, -10),
    FillOperation.Replace
    )
    mobs.give(
    mobs.target(ALL_PLAYERS),
    BOW,
    1
    )
    mobs.give(
    mobs.target(ALL_PLAYERS),
    ARROW,
    1
    )
    startShootOut()
})
// deze code zorgt er voor de dat pvp niet aan gaat in het begin, en dan na 5 seconden wel
// het stuurt ook een event naar de datapack dat dan de spelers teleporteert naar de juiste plek
function startShootOut () {
    player.execute(
    "/scriptevent codefever:start-shoot-out " + "{" + ("\"x\":" + player.position().getValue(Axis.X) + ",") + ("\"y\":" + player.position().getValue(Axis.Y) + ",") + ("\"z\":" + player.position().getValue(Axis.Z)) + "}"
    )
    player.execute(
    "gamerule pvp false"
    )
    player.say("§aShootout start binnen 5 seconden!")
    loops.pause(2000)
    player.say("§a3 seconden!")
    loops.pause(1000)
    player.say("§a2 seconden!")
    loops.pause(1000)
    player.say("§a1 second!")
    loops.pause(1000)
    player.say("§aStart!")
    player.execute(
    "gamerule pvp true"
    )
}

```

## Spleef

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je Spleef maakt.

[Klik hier om naar het leerplatform te gaan](https://leerplatform.codefever.be/).
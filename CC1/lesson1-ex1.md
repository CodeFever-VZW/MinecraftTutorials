# Missie 1

```blocks

player.onChat("oef6", function () {
    agent.move(FORWARD, 6)
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 3)
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 5)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 2)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 10)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 10)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 10)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 3)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 2)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 2)
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 1)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 2)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 2)
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 6)
})
```

```template
player.onChat("start", function() {
    zetKlaar();
})

/**
 *Dit blokje moet je niet programmeren.
 */
function zetKlaar() {
    agent.teleport(world(87, 72, -28), EAST);
}
```

## Agent Testen

Gebruik het leerplatform om de oefeningen op te lossen
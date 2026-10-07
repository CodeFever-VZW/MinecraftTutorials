# MC Reeks 3 Les 8

```template
player.onChat("valAan", function () {})
player.onChat("stop", function () {})
```

```block
  agent.turn(LEFT_TURN)
    agent.teleportToPlayer()
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
    agent.teleport(pos(LEFT_TURN, FORWARD, 0), WEST)
    agent.teleport(pos(agent.inspect(AgentInspection.Block, FORWARD), 0, 0), WEST)
    agent.setAssist(PLACE_ON_MOVE, agent.detect(AgentDetection.Block, FORWARD))
    agent.place(FORWARD)
    agent.interact(FORWARD)
    agent.destroy(FORWARD)
    agent.till(FORWARD)
    agent.attack(FORWARD)
    agent.attack(FORWARD)
    agent.collectAll()
    agent.collect(IRON_SHOVEL)
    agent.setSlot(1)
    agent.setItem(GRASS, agent.getItemCount(agent.getItemSpace(1)), 1)
    agent.dropAll(FORWARD)
    agent.transfer(agent.getItemDetail(1), 1, 2)
let valaan = 0
player.onChat("jump", function () {
    agent.teleport(world(0, 0, 0), WEST)
    valaan = 0
    while (valaan == randint(0, 10)) {
    	
    }
    agent.attack(FORWARD)
    if (true) {
        agent.turn(LEFT_TURN)
    }
    for (let index = 0; index < 4; index++) {
    	
    }
    agent.move(FORWARD, 1)
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
})

```

## Kill the zombie pigman
Gebruik je agent om de zombie pigmans te doden.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Kill the zombie pigman](https://codefeverpublic.blob.core.windows.net/public-content/images/8be11a9754c20977a0eed8381a68115f81ac61c696ff48abbe83503fa9724154.png)
    

## Zelf de put in gaan
In het midden verschijnt een knop. Bouw eerst iets zodat je veilig de put in kan.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Zelf de put in gaan](https://codefeverpublic.blob.core.windows.net/public-content/images/722506727c3196027bd7529c322ca56ad2f776224d0c374e5a446607cdada59b.png)

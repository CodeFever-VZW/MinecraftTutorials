# Minecraft 3 les 2

```template
let Klaar = 0;
player.onChat("stop", function () {
    Klaar = 1;
});
player.onChat("level1", function () {
    player.say(":)")
    agent.teleport(world(-86, 66, 325), NORTH)
    while (!(agent.detect(AgentDetection.Redstone, DOWN))) {
        if (!(agent.detect(AgentDetection.Block, RIGHT))) {
            agent.turn(RIGHT_TURN)
            agent.move(FORWARD, 1)
        } else if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else if (!(agent.detect(AgentDetection.Block, LEFT))) {
            agent.turn(LEFT_TURN)
            agent.move(FORWARD, 1)
        } else {
            agent.turn(RIGHT_TURN)
            agent.turn(RIGHT_TURN)
        }
    }
})
player.onChat("level2", function () {
    player.say(":)")
    Klaar = 0
    agent.teleport(world(-85, 66, 285), NORTH)
    while (Klaar == 0) {
        if (!(agent.detect(AgentDetection.Block, RIGHT))) {
            agent.turn(RIGHT_TURN)
            agent.move(FORWARD, 1)
        } else if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else if (!(agent.detect(AgentDetection.Block, LEFT))) {
            agent.turn(LEFT_TURN)
            agent.move(FORWARD, 1)
        } else {
            agent.turn(RIGHT_TURN)
            agent.turn(RIGHT_TURN)
            agent.move(FORWARD, 1)
        }
    }
})
function plaatsBrugBlok () {
    agent.setItem(POLISHED_GRANITE, 64, 1)
    if (!(agent.detect(AgentDetection.Block, UP))) {
        agent.place(UP)
    }
}
player.onChat("level3", function () {
    player.say(":)")
    Klaar = 0
    agent.teleport(world(-84, 67, 224), NORTH)
    plaatsBrugBlok()
    while (Klaar == 0) {
        agent.move(RIGHT, 1)
        if (agent.detect(AgentDetection.Redstone, DOWN)) {
            agent.turn(RIGHT_TURN)
            plaatsBrugBlok()
        } else {
            agent.move(LEFT, 1)
            agent.turn(LEFT_TURN)
        }
    }
})

```

```blocks
let Klaar = 0
player.onChat("stop", function () {
    Klaar = 1;
});
player.onChat("level1", function () {
    agent.teleport(world(-86, 66, 325), NORTH)
    Klaar = 0
    while (Klaar == 0) {
        if (agent.detect(AgentDetection.Redstone, DOWN)) {
            Klaar = 1
            player.teleport(agent.getPosition())
        }
        if (!(agent.detect(AgentDetection.Block, RIGHT))) {
            agent.turn(RIGHT_TURN)
            agent.move(FORWARD, 1)
        } else if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else if (!(agent.detect(AgentDetection.Block, LEFT))) {
            agent.turn(LEFT_TURN)
            agent.move(FORWARD, 1)
        } else {
            agent.turn(RIGHT_TURN)
            agent.turn(RIGHT_TURN)
        }
    }
})
player.onChat("level2", function () {
    agent.teleport(world(-85, 66, 285), NORTH)
    Klaar = 0
    while (Klaar == 0) {
        agent.setItem(TORCH, 10, 1)
        if (agent.detect(AgentDetection.Redstone, DOWN)) {
            Klaar = 1
            player.teleport(agent.getPosition())
        }
        if (!(agent.detect(AgentDetection.Block, RIGHT))) {
            agent.setSlot(1)
            agent.place(DOWN)
            agent.turn(RIGHT_TURN)
            agent.move(FORWARD, 1)
        } else if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else if (!(agent.detect(AgentDetection.Block, LEFT))) {
            agent.setSlot(1)
            agent.place(DOWN)
            agent.turn(LEFT_TURN)
            agent.move(FORWARD, 1)
        } else {
            agent.turn(RIGHT_TURN)
            agent.turn(RIGHT_TURN)
        }
    }
});
function plaatsBrugBlok () {
    if (!(agent.detect(AgentDetection.Block, UP))) {
        agent.place(UP)
    }
}
player.onChat("level3", function () {
    player.say(":)")
    agent.setItem(POLISHED_GRANITE, 64, 1)
    agent.teleport(world(-84, 67, 224), NORTH)
    plaatsBrugBlok()
    while (klaar !== 0) {
        agent.move(RIGHT, 1)
        if (agent.detect(AgentDetection.Redstone, DOWN)) {
            agent.turn(RIGHT_TURN)
            plaatsBrugBlok()
        } else {
            agent.move(LEFT, 1)
            agent.move(FORWARD, 1)
            if (agent.detect(AgentDetection.Redstone, DOWN)) {
                plaatsBrugBlok()
            } else {
                agent.move(BACK, 1)
                agent.move(LEFT, 1)
                if (agent.detect(AgentDetection.Redstone, DOWN)) {
                    agent.turn(LEFT_TURN)
                    plaatsBrugBlok()
                } else {
                    agent.move(RIGHT, 1)
                    agent.turn(LEFT_TURN)
                    agent.turn(LEFT_TURN)
                    agent.move(FORWARD, 1)
                }
            }
        }
    }
})
```

## Level 1

Laat je agent het doolhof oplossen. Gebruik de rechter hand regel.

Meer uitleg kan je vinden in de slides van het leerplatform.

## Level 2

Kopier je code en pas ze aan voor level 2. Je moet nu 3 drukplaten activeren.

Meer uitleg kan je vinden in de slides van het leerplatform.

## Level 3

Gebruik de agent om voor jou de veilige weg door de lava te zoeken en laat hem een brug bouwen waar je veilig over kan.

Meer uitleg kan je vinden in de slides van het leerplatform.
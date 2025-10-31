# MC Reeks 1 Les 9

```template
let hoogte = 0
player.onChat("coolViaduct", function () {
    agent.teleportToPlayer()
    agent.setSlot(1)
    agent.move(UP, 10)
    for (let index = 0; index < 3; index++) {
        agent.setSlot(1)
        agent.place(RIGHT)
        agent.move(UP, 1)
        agent.setSlot(4)
        agent.place(RIGHT)
        agent.move(DOWN, 1)
        agent.setSlot(1)
        hoogte = 0
        while (!(agent.detect(AgentDetection.Block, DOWN))) {
            agent.move(DOWN, 1)
            agent.place(UP)
            hoogte += 1
        }
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
        }
        agent.move(FORWARD, 1)
        agent.place(BACK)
        for (let index = 0; index < hoogte; index++) {
            if (agent.detect(AgentDetection.Block, UP)) {
                agent.destroy(UP)
            }
            agent.move(UP, 1)
        }
        for (let index = 0; index < 4; index++) {
            agent.move(FORWARD, 1)
            agent.place(BACK)
        }
    }
    agent.move(RIGHT, 1)
    agent.place(BACK)
    agent.move(UP, 1)
    agent.setSlot(4)
    agent.place(BACK)
    agent.move(LEFT, 1)
    agent.move(BACK, 1)
    agent.move(BACK, 1)
    agent.setSlot(3)
    agent.place(FORWARD)
    agent.setSlot(2)
    while (agent.detect(AgentDetection.Block, DOWN)) {
        agent.move(BACK, 1)
        agent.place(FORWARD)
    }
})
player.onChat("viaduct1", function () {
    agent.teleportToPlayer()
    agent.move(UP, 10)
    for (let index = 0; index < 3; index++) {
        hoogte = 0
        while (!(agent.detect(AgentDetection.Block, DOWN))) {
            agent.move(DOWN, 1)
            agent.setSlot(1)
            agent.place(UP)
            hoogte += 1
        }
        agent.move(FORWARD, 1)
        agent.setSlot(1)
        agent.place(BACK)
        agent.move(UP, hoogte)
        for (let index = 0; index < 4; index++) {
            agent.move(FORWARD, 1)
            agent.setSlot(1)
            agent.place(BACK)
        }
    }
})
player.onChat("stelAgentIn2", function () {
    agent.teleportToPlayer()
    agent.setItem(BRICKS, 64, 1)
    agent.setItem(POWERED_RAIL, 64, 2)
    agent.setItem(MINECART_WITH_T_N_T, 64, 3)
    agent.setItem(ACTIVATOR_RAIL, 64, 4)
    agent.setItem(REDSTONE_TORCH, 64, 5)
    agent.setItem(REDSTONE_WIRE, 64, 10)
    agent.setItem(REDSTONE_LAMP, 64, 11)
    agent.setItem(LEVER, 64, 12)
})
player.onChat("stelAgentIn", function () {
    agent.teleportToPlayer()
    agent.setItem(BRICKS, 64, 1)
    agent.setItem(POWERED_RAIL, 64, 2)
    agent.setItem(ACTIVATOR_RAIL, 64, 3)
    agent.setItem(REDSTONE_TORCH, 64, 4)
})
player.onChat("nachtlampen", function () {
    gameplay.timeSet(gameplay.time(MIDNIGHT))
    agent.teleportToPlayer()
    agent.setSlot(12)
    agent.place(BACK)
    agent.setSlot(10)
    for (let index = 0; index < 3; index++) {
        agent.move(FORWARD, 1)
        agent.place(BACK)
    }
    for (let index = 0; index < 3; index++) {
        agent.move(LEFT, 1)
        agent.place(RIGHT)
    }
    agent.setSlot(11)
    agent.move(RIGHT, 1)
    agent.place(LEFT)
    agent.setSlot(10)
    agent.move(RIGHT, 2)
    for (let index = 0; index < 3; index++) {
        agent.move(RIGHT, 1)
        agent.place(LEFT)
    }
    agent.setSlot(11)
    agent.move(RIGHT, 1)
    agent.place(LEFT)
})
player.onChat("viaduct1beter", function () {
    agent.teleportToPlayer()
    agent.setSlot(1)
    agent.move(UP, 10)
    for (let index = 0; index < 3; index++) {
        hoogte = 0
        while (!(agent.detect(AgentDetection.Block, DOWN))) {
            agent.move(DOWN, 1)
            agent.place(UP)
            hoogte += 1
        }
        agent.move(FORWARD, 1)
        agent.place(BACK)
        agent.move(UP, hoogte)
        for (let index = 0; index < 4; index++) {
            agent.move(FORWARD, 1)
            agent.place(BACK)
        }
    }
})
player.onChat("viaduct1fase2", function () {
    agent.teleportToPlayer()
    agent.setSlot(1)
    agent.move(UP, 10)
    for (let index = 0; index < 3; index++) {
        hoogte = 0
        while (!(agent.detect(AgentDetection.Block, DOWN))) {
            agent.move(DOWN, 1)
            agent.place(UP)
            hoogte += 1
        }
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
        }
        agent.move(FORWARD, 1)
        agent.place(BACK)
        for (let index = 0; index < hoogte; index++) {
            if (agent.detect(AgentDetection.Block, UP)) {
                agent.destroy(UP)
            }
            agent.move(UP, 1)
        }
        for (let index = 0; index < 4; index++) {
            agent.move(FORWARD, 1)
            agent.place(BACK)
        }
    }
})
```

```block
let hoogte = 0
player.onChat("coolViaduct", function () {
    agent.teleportToPlayer()
    agent.setSlot(1)
    agent.move(UP, 10)
    for (let index = 0; index < 3; index++) {
        agent.setSlot(1)
        agent.place(RIGHT)
        agent.move(UP, 1)
        agent.setSlot(4)
        agent.place(RIGHT)
        agent.move(DOWN, 1)
        agent.setSlot(1)
        hoogte = 0
        while (!(agent.detect(AgentDetection.Block, DOWN))) {
            agent.move(DOWN, 1)
            agent.place(UP)
            hoogte += 1
        }
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
        }
        agent.move(FORWARD, 1)
        agent.place(BACK)
        for (let index = 0; index < hoogte; index++) {
            if (agent.detect(AgentDetection.Block, UP)) {
                agent.destroy(UP)
            }
            agent.move(UP, 1)
        }
        for (let index = 0; index < 4; index++) {
            agent.move(FORWARD, 1)
            agent.place(BACK)
        }
    }
    agent.move(RIGHT, 1)
    agent.place(BACK)
    agent.move(UP, 1)
    agent.setSlot(4)
    agent.place(BACK)
    agent.move(LEFT, 1)
    agent.move(BACK, 1)
    agent.move(BACK, 1)
    agent.setSlot(3)
    agent.place(FORWARD)
    agent.setSlot(2)
    while (agent.detect(AgentDetection.Block, DOWN)) {
        agent.move(BACK, 1)
        agent.place(FORWARD)
    }
})
player.onChat("viaduct1", function () {
    agent.teleportToPlayer()
    agent.move(UP, 10)
    for (let index = 0; index < 3; index++) {
        hoogte = 0
        while (!(agent.detect(AgentDetection.Block, DOWN))) {
            agent.move(DOWN, 1)
            agent.setSlot(1)
            agent.place(UP)
            hoogte += 1
        }
        agent.move(FORWARD, 1)
        agent.setSlot(1)
        agent.place(BACK)
        agent.move(UP, hoogte)
        for (let index = 0; index < 4; index++) {
            agent.move(FORWARD, 1)
            agent.setSlot(1)
            agent.place(BACK)
        }
    }
})
player.onChat("stelAgentIn2", function () {
    agent.teleportToPlayer()
    agent.setItem(BRICKS, 64, 1)
    agent.setItem(POWERED_RAIL, 64, 2)
    agent.setItem(MINECART_WITH_T_N_T, 64, 3)
    agent.setItem(ACTIVATOR_RAIL, 64, 4)
    agent.setItem(REDSTONE_TORCH, 64, 5)
    agent.setItem(REDSTONE_WIRE, 64, 10)
    agent.setItem(REDSTONE_LAMP, 64, 11)
    agent.setItem(LEVER, 64, 12)
})
player.onChat("stelAgentIn", function () {
    agent.teleportToPlayer()
    agent.setItem(BRICKS, 64, 1)
    agent.setItem(POWERED_RAIL, 64, 2)
    agent.setItem(ACTIVATOR_RAIL, 64, 3)
    agent.setItem(REDSTONE_TORCH, 64, 4)
})
player.onChat("nachtlampen", function () {
    gameplay.timeSet(gameplay.time(MIDNIGHT))
    agent.teleportToPlayer()
    agent.setSlot(12)
    agent.place(BACK)
    agent.setSlot(10)
    for (let index = 0; index < 3; index++) {
        agent.move(FORWARD, 1)
        agent.place(BACK)
    }
    for (let index = 0; index < 3; index++) {
        agent.move(LEFT, 1)
        agent.place(RIGHT)
    }
    agent.setSlot(11)
    agent.move(RIGHT, 1)
    agent.place(LEFT)
    agent.setSlot(10)
    agent.move(RIGHT, 2)
    for (let index = 0; index < 3; index++) {
        agent.move(RIGHT, 1)
        agent.place(LEFT)
    }
    agent.setSlot(11)
    agent.move(RIGHT, 1)
    agent.place(LEFT)
})
player.onChat("viaduct1beter", function () {
    agent.teleportToPlayer()
    agent.setSlot(1)
    agent.move(UP, 10)
    for (let index = 0; index < 3; index++) {
        hoogte = 0
        while (!(agent.detect(AgentDetection.Block, DOWN))) {
            agent.move(DOWN, 1)
            agent.place(UP)
            hoogte += 1
        }
        agent.move(FORWARD, 1)
        agent.place(BACK)
        agent.move(UP, hoogte)
        for (let index = 0; index < 4; index++) {
            agent.move(FORWARD, 1)
            agent.place(BACK)
        }
    }
})
player.onChat("viaduct1fase2", function () {
    agent.teleportToPlayer()
    agent.setSlot(1)
    agent.move(UP, 10)
    for (let index = 0; index < 3; index++) {
        hoogte = 0
        while (!(agent.detect(AgentDetection.Block, DOWN))) {
            agent.move(DOWN, 1)
            agent.place(UP)
            hoogte += 1
        }
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
        }
        agent.move(FORWARD, 1)
        agent.place(BACK)
        for (let index = 0; index < hoogte; index++) {
            if (agent.detect(AgentDetection.Block, UP)) {
                agent.destroy(UP)
            }
            agent.move(UP, 1)
        }
        for (let index = 0; index < 4; index++) {
            agent.move(FORWARD, 1)
            agent.place(BACK)
        }
    }
})


```

## Viaduct

Kijk op het [leerplatform](https://leerplatform.codefever.be/) hoe je het viaduct maakt.

[Klik hier om naar het leerplatform te gaan](https://leerplatform.codefever.be/).
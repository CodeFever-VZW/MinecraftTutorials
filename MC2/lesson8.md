# Minecraft 2 les 8

```template
function startLevel () {

}

function checkLevel () {
    
}

function level1 () {
    
}

player.onChat("horde", function () {
    level = 1
    gameplay.setDifficulty(EASY)
    killAllMobs()
    startLevel()
})

mobs.onMobKilled(mobs.monster(ZOMBIE), function () {
    horde += -1
    checkLevel()
})

function killAllMobs () {
    selector = mobs.target(ALL_ENTITIES)
    selector.addRule("type", "!player")
    mobs.kill(
    selector
    )
}


```

```blocks
let horde = 0
let selector: TargetSelector = null
let level = 0
function level4 () {
    horde = 20
    spawnZombie(5)
    spawnSpinnen(10)
    spawnCreepers(5)
}
function level1 () {
    horde = 10
    spawnZombie(10)
}
function level3 () {
    horde = 20
    spawnZombie(10)
    spawnSpinnen(10)
}
mobs.onMobKilled(mobs.monster(CREEPER), function () {
    horde += -1
    checkLevel()
})
function level2 () {
    horde = 15
    spawnZombie(10)
}
function killAllMobs () {
    selector = mobs.target(ALL_ENTITIES)
    selector.addRule("type", "!player")
    mobs.kill(
    selector
    )
}
player.onChat("horde", function () {
    level = 1
    gameplay.setDifficulty(EASY)
    startLevel()
    killAllMobs()
})
function randomLocatie () {
    return randpos(
    world(13, -60, 13),
    world(-13, -60, -13)
    )
}
function spawnCreepers (aantal: number) {
    for (let index = 0; index < aantal; index++) {
        mobs.spawn(mobs.monster(CREEPER), randomLocatie())
    }
}
function spawnSpinnen (aantal: number) {
    for (let index = 0; index < aantal; index++) {
        mobs.spawn(mobs.monster(SPIDER), randomLocatie())
    }
}
mobs.onMobKilled(mobs.monster(SPIDER), function () {
    horde += -1
    checkLevel()
})
function spawnZombie (aantal: number) {
    for (let index = 0; index < aantal; index++) {
        mobs.spawn(mobs.monster(ZOMBIE), randomLocatie())
    }
}
function checkLevel () {
    if (horde <= 0) {
        killAllMobs()
        level += 1
        startLevel()
        player.say("Volgend level!")
    } else {
        player.say("" + horde + " Monster over")
    }
}
mobs.onMobKilled(mobs.monster(ZOMBIE), function () {
    horde += -1
    checkLevel()
})
function startLevel () {
    if (level == 1) {
        level1()
    } else if (level == 2) {
        level2()
    } else if (level == 3) {
        level3()
    } else if (level == 4) {
        level4()
    } else {
    	
    }
}

```

## Leerplatform

Gebruik het leerplatform om de oefening op te lossen.

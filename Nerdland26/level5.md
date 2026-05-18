# Nerdland 26

```template
player.onChat("start", function () {
    
})
```

```block
player.onChat("start", function () {
    agent.teleport(world(-25, -60, 40), SOUTH)
    for (let index = 0; index < 6; index++) {
        agent.move(FORWARD, 1)
    }
})

agent.turn(LEFT_TURN)
```

## Level 5

Net zoals bij de vorige opdracht moet je de agent van het gouden blok tot het emerald (lichtgroene) blok laten gaan. Je mag terug kiezen hoe je dit doet. De agent zal automatisch een lijn trekken op de blokken waar hij over gaat. 

De Agent kan enkel een lijn trekken op de donker groene blokken.

Verbind het gouden en groene blok om het leevel te voltooien. Je kan de opdracht starten door "start" te zeggen in de chat.
# MC Reeks 3 Les 4

```template
function zetVariabelenKlaar(){
    let startX = 55;
    let startY = 70;
    let startZ = 0;
};
function tribune1(){};
function tribune2(){};
function tribune3(){};
function tribune4(){};
function snakePit(){};

player.onChat("tribune", function () {
    zetVariabelenKlaar();
    snakePit();
    tribune1();
    tribune2();
    tribune3();
    tribune4();
    player.say("Klaar met bouwen!");
});
```

```block
let index = 0
blocks.onBlockBroken(GRASS, function () {
    agent.turn(LEFT_TURN)
})
player.onChat("run", function () {
    for (let index = 0; index <= 4; index++) {
        blocks.fill(
        GRASS,
        world(0, 0, 0),
        pos(index + 0, 0, 0),
        FillOperation.Replace
        )
    }
    blocks.place(GRASS, pos(0, 0, 0))
    for (let index2 = 0; index2 < 4; index2++) {
        player.say(":)")
    }
    index = 0
    while (0 == 0 == "") {
        doSomething()
    }
    if (!true) {

    }
    index += 1
    mobs.spawn(CHICKEN, agent.getPosition())
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
})
function doSomething () {

}

```

## Snakepit

Gebruik zeker de startcoördinaten!

Als er iets mis gaat kan je het reset item gebruiken om opnieuw te proberen.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Snakepit](https://codefeverpublic.blob.core.windows.net/public-content/images/b2d975509d6804759ee55656470bbdd16f4a313ad6b20be26e859ebd6b2a020b.png)

## Tribune

Begin bij tribune 1.
Gebruik de functies en vul je code hier in.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Tribune](https://codefeverpublic.blob.core.windows.net/public-content/images/e4218de35048b39365a820be94ffafa268915ab84f065b7e70681a0084422692.png)

## Meerdere tribunes

Werk verder aan Tribunes 2, 3 en 4.
Gebruik de functies en pas je code aan voor de nieuwe tribunes.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Meerdere tribunes](https://codefeverpublic.blob.core.windows.net/public-content/images/9d70747c652666f1aa0673c510fee15b9d0d2bfbda0507da9b6937b4582e72d2.png)

## Gesloten arena

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Gesloten arena](https://codefeverpublic.blob.core.windows.net/public-content/images/2f009506689aa1024161faa11549e82c3b81ffc1c2c5d0d770a15e74260ed62e.png)

## Uitgang (Extra)

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Uitgang](https://codefeverpublic.blob.core.windows.net/public-content/images/662d69c23abe031d6e089378da7c45ace73c03e8fea5ee2658b930d50f1bfcfb.png)

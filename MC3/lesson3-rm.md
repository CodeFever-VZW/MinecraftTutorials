# MC Reeks 3 Les 3

```template
player.onChat("level1", function () {});
player.onChat("level2", function () {});
player.onChat("level3", function () {});

function vervangBlok(){};

function zetKlaar(){
    builder.teleportTo(world(-158, 69, -908));
    builder.face(SOUTH);
}
```

```block
//level 1
player.onChat("level1", function () {
    zetKlaar();
    for (let index = 0; index < 10; index++) {
        vervangBlok()
        builder.move(FORWARD, 4)
    }
});

function vervangBlok () {
    if (blocks.testForBlock(YELLOW_WOOL, builder.position())) {
        blocks.place(GOLD_BLOCK, builder.position())
    } else if (blocks.testForBlock(RED_WOOL, builder.position())) {
        blocks.place(REDSTONE_BLOCK, builder.position())
    } else if (blocks.testForBlock(BLUE_WOOL, builder.position())) {
        blocks.place(LAPIS_LAZULI_BLOCK, builder.position())
    } else if (blocks.testForBlock(LIME_WOOL, builder.position())) {
        blocks.place(EMERALD_BLOCK, builder.position())
    }
}

//level 2
player.onChat("level2", function () {
    zetKlaar();
    for (let index = 0; index < 10; index++) {
        for (let index = 0; index < 10; index++) {
            vervangBlok()
            builder.move(FORWARD, 4)
        }
        builder.move(BACK, 40)
        builder.move(LEFT, 4)
    }
});

//level 3
player.onChat("level1", function () {
    zetKlaar();
    for (let index = 0; index < 3; index++) {
        for (let index = 0; index < 10; index++) {
            for (let index = 0; index < 10; index++) {
                vervangBlok()
                builder.move(FORWARD, 4)
            }
            builder.move(BACK, 40)
            builder.move(LEFT, 4)
        }
        builder.move(RIGHT, 40)
        builder.move(DOWN, 4)
    }
});

function zetKlaar(){
    builder.teleportTo(world(-158, 69, -908));
    builder.face(SOUTH);
}

```

## Level 1

De bouwer moet over alle gekleurde wol blokken gaan en ze vervangen door het juiste mineraal.
Uitleg over de code en de mineralen kan je vinden op het leerplatform

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

![Level 1](https://codefeverpublic.blob.core.windows.net/public-content/images/d8f2f1d0aa1cb23583ac9bae42084e903b7bcc2e059774f9ca52129147fb13f4.png)

## Level 2

Programmeer de bouwer om de 20 goudblokken te vinden.

Kijk op het [leerplatform](https://leerplatform.codefever.be/) voor meer uitleg.

# Brainybot

## Introduction

Brainybot is designed to teach computer science fundamentals using either JavaScript, Python, or a scratch-like block coding language. The accompanying curriculum has modules that slot into the existing CSTA standards for middle schools, and the code.org AP CSP curriculum for high schools. Each student gets their own robot. 

Features include: 
- 2 wheels for movement
- Movable head
- Proximity / distance sensor on head
- Color sensors on bottom, to detect black lines and the edge of the sumo ring
- Music generator
- 2-way radio communication with other nearby Brainybots 
- Programmable in JavaScript, Python, and the Microsoft Makecode block language environment
- Powered by BBC micro:bit. 

[Purchase link](https://afterschoolrobotics.com/store/p/brainybot)

[Curriculum link](https://drive.google.com/drive/folders/1k4ZVxxIk2RaNHjFOI__wTaOOR8qrL3-G?usp=sharing)


## Basic Commands

* Blinking LED

```
bb.I2CInit()
music.startMelody(music.builtInMelody(Melodies.Dadadadum), MelodyOptions.Forever)
bb.controlMotor(bb.MyEnumMotor.AllMotor, bb.MyEnumDir.Forward, 255)
basic.forever(function () {
    bb.setIndexColor(bb.ledRange(0, 3), bb.NeoPixelColors.Red)
    basic.pause(1000)
    bb.setIndexColor(bb.ledRange(0, 3), bb.NeoPixelColors.Blue)
    basic.pause(1000)
})
```
* Light Sensing Robot
```
bb.I2CInit()
basic.forever(function () {
    basic.showNumber(input.lightLevel())
})
```

## License

MIT

## Supported targets

* for PXT/microbit


```package
Brainybot=github:afterschoolrobotics/pxt-brainybot
```

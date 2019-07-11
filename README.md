
# eboticsMIBO Package
This ebotics MIBO package was developed by [ebotics](https://www.ebotics.com/) 

The ebotics MIBO is a your first robot DIY robot for the BBC micro:bit. The MIBO extends the micro:bit's 3 GPIO ports and allow for different sensors and components to be easily attached to the micro:bit. A basic ebotics MIBO can be easily programmed to run autonomously, with a remote control, and even create rainbow beacons of light. Just add one of the many extensions available and your ebotics MIBO can do even more things like line and light following, obstacle avoiding, drawing and more!  




## Code Example
```JavaScript

let strip: neopixel.Strip = null
eboticsMIBO.init_wheel(AnalogPin.P1, AnalogPin.P2)
strip = neopixel.create(DigitalPin.P0, 24, NeoPixelMode.RGB)
strip.showRainbow(1, 360)
basic.showIcon(IconNames.Heart)
basic.forever(function () {
    strip.rotate(1)
    basic.pause(100)
    strip.show()
})
basic.forever(function () {
    eboticsMIBO.freestyle(30, 90)
    basic.pause(1500)
    eboticsMIBO.freestyle(90, 30)
    basic.pause(1500)
})


```

## License
MIT

## Supported targets
for PXT/microbit (The metadata above is needed for package search.)


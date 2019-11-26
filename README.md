
# eboticsMIBO Package
This ebotics MIBO package was developed by [ebotics](https://www.ebotics.com/product/mibo/) 

ebotics MIBO is your first robot with the BBC micro:bit electronic board. MIBO extends the micro:bit's 3 GPIO ports, allowing different sensors and components to be easily attached to the micro:bit. Add the eboticsMIBO extension and program MIBO to follow a line, draw, dance, light in different colors and much more!

For more information on MIBO, please consult the following [link](https://www.ebotics.com/product/mibo/#guides)

![](https://i.imgur.com/vTegCSm.png)


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


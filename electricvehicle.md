# Green Wheels in Motion 
```package
fwd-edu-breakout=github:climate-action-kits/pxt-fwd-edu/fwd-breakout
```
## 
``||Step 1||`` 
On your screen you can see an ``||basic: on start||`` block and a ``||basic:forever||``
block. Insert or nest a ``||basic: show leds||`` under the ``||basic:on start||``.
Click on the boxes of the ``||basic:show leds||`` to turn the ``||basic:leds||``
ON or OFF. Let's try to write ``||Hi||`` by turning on the ``||basic:leds||`` of the 
``||basic:show leds||`` blocks. Click on the blub to show your hint.
```blocks
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
```
## 
``||Step 2||``
Click on the ``||input:input||`` drawer. 
Find the ``||input: on button A pressed||`` block. Drag the block and place it 
on the coding screen.
Click on the blub to show your hint.
```blocks
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
input.onButtonPressed(Button.A, function () {
})
```
## 
``||Step 3||``
Click on the ``||input:input||`` drawer. 
Find the ``||input: on button A pressed||`` block. Drag the block and place it 
on the coding screen. This time change ``||input:A||`` to ``||input:B||``
Click on the blub to show your hint.
```blocks
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
input.onButtonPressed(Button.A, function () {
})
input.onButtonPressed(Button.B, function () {
})
```
## 
``||Step 4||``
The two buttons ``||input:A||`` and ``||input:B||`` will control the operation of the
the ``||Green Electric Vehicle||``. To run the ``||Electric Vehicle||`` ``||input: Button A||``
will be used. Next go to ``||fwdMotors:Motors||`` drawer and find 
``||fwdMotors:Setup Driving||`` drag this block and nest it under ``||basic:on start||``
Select ``||fwdMotors: servo 1 and servo 2||`` for the ``||fwdMotors: Setup Driving||`` block

Click on the blub to show your hint.
```blocks
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
fwdMotors.setupDriving(
fwdMotors.servo1,
fwdMotors.servo2
)
input.onButtonPressed(Button.A, function () {
    })
input.onButtonPressed(Button.B, function () {
})
```
## 
``||Step 5||``
Under button ``||input:A||`` nest ``||fwdMotors: Drive forward at 50||`` this will
control the forward operation of the
the ``||Green Electric Vehicle||``. 
Click on the blub to show your hint.
```blocks
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
fwdMotors.setupDriving(
fwdMotors.servo1,
fwdMotors.servo2
)
input.onButtonPressed(Button.A, function () {
    fwdMotors.drive(fwdMotors.drivingDirection.forward, 50)
})
input.onButtonPressed(Button.B, function () {
})
```
## 
``||Step 6||``
The ``||input:Button B||`` is used for stopping the ``||Green Electric Vehicle||``. From the
``||fwdMotors:Motors||`` drawer drag the ``||fwdMotors:Stop Motors||`` block
and nest it under ``||input:on button B pressed||`` block. 
Click on the blub to show your hint.
```blocks
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
input.onButtonPressed(Button.A, function () {
   fwdMotors.drive(fwdMotors.drivingDirection.forward, 50)
})
input.onButtonPressed(Button.B, function () {
    fwdMotors.stop()
})
```
## @showhint 
This is the final code. On pressing ``||input: Button A||`` should make your ``||Green Electric Vehicle||``
move forward and when ``||input: Button B||`` is pressed the ``||Green Electric Vehicle||`` stops.
```blocks
input.onButtonPressed(Button.A, function () {
    fwdMotors.drive(fwdMotors.drivingDirection.forward, 50)
})
input.onButtonPressed(Button.B, function () {
    fwdMotors.stop()
})
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
fwdMotors.setupDriving(
fwdMotors.servo1,
fwdMotors.servo2
)
basic.forever(function () {
	
})

```
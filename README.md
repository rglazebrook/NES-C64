# NES-C64

![NES-C64 Rev. B Front](https://user-images.githubusercontent.com/2517006/123490250-4eb47180-d5d9-11eb-9ce5-ce7d04e8b65b.png)

![NES-C64 Rev. B Back](https://user-images.githubusercontent.com/2517006/123552846-c3a0bc00-d73d-11eb-8a33-db70692672ee.png)

The NES-C64 (a play on the NES-004 model number of the original controller) is a non-destructive drop-in replacement PCB to convert an original NES-004 controller to a Commodore 64 controller. Once the board is put together, you simply open the original NES controller, remove the PCB and cable, and then add the new board and cable. If you ever want to convert the controller back to NES use, it's as simple as reversing the process.

## But, Why?
I may be sadistic, but I'm a big fan of the original NES controller. I grew up with one and it feels natural to me. So (much) later in life, when I got a Commodore 64 and tried to play platformer games using the C64 joystick, I found myself unimpressed and wishing I had a controller in my hand.

My first effort was to rewire an NES controller with a new cable but reuse the original PCB. While this works, it does require desoldering an existing cable and chip, and that feels more destructive than I wanted. Surely someone has a way to just drop in a new PCB so I don't have to hurt the old one?

After doing literal HOURS(!) of Google searches, I couldn't find anything that fit the bill. So I downloaded KiCad, watched a bunch of tutorials, and here we are.

## Features

 * Completely non-destructive modification of the original NES controller.
 * Uses relatively available parts (the cable seems to be the most complicated bit to find).
 * All buttons are used!
   * Up/Down/Left/Right are as expected
   * B is fire
   * Pressing Select sets A to "jump" (Up) mode
   * Pressing Start sets A to "fire" mode

## Instructions
 1. Get the PCB printed (I used ![JLCPCB](https://jlcpcb.com/), because their online interface was very nice and their prices were totally reasonable)
 2. Order the components (see the bill of materials below)
 3. Solder everything together (I go shortest to tallest: resistors, 556 IC, transistors, cable)
 4. Unscrew the back of the NES-004 controller
 5. Pull out the existing PCB and cable, and store it somewhere safe
 6. Drop in the news PCB and cable, and route the cable out of the way and through the opening at the top
 7. Enjoy!

### Bill of Materials (BOM)
 * 2 - ![10K Ohm, 1/4W resistors](https://www.mouser.com/ProductDetail/ohmite/ok1035e-r52/?qs=xrm8qtdNeVNEKDgGXbVwvg%3D%3D&countrycode=US&currencycode=USD)
 * 2 - ![220 Ohm, 1/4W resistors](https://www.mouser.com/ProductDetail/ohmite/ok2215e-r52/?qs=AkUtuiJmyfmB6duDjv7E8w%3D%3D&countrycode=US&currencycode=USD)
 * 2 - ![NPN transistors](https://www.mouser.com/ProductDetail/rectron/2n5551-t/?qs=oFjv9VeDysEhdg04%252bKG5qg%3D%3D&countrycode=US&currencycode=USD)
 * 1 - ![NE556 timer](https://www.mouser.com/ProductDetail/texas-instruments/ne556n/?qs=gb35HGp1gQKUkn%252b6zgU6RA%3D%3D&countrycode=US&currencycode=USD)
 * 1 - ![DE9 cable](https://console5.com/store/atari-sega-commodore-coleco-msx-6-1-8m-joystick-controller-project-repair-cable-cord.html)

## Caveats and Gotchas
 1. After assembling, my start button didn't want to engage. I solved this by added a bit of ![conductive copper tape](https://smile.amazon.com/gp/product/B01MR5DSCM/) to the bottom of the button to increase conductivity; after that, everything worked perfectly.
 2. Be sure that the components are on the _opposite_ side of the board as the button contacts. This ensures there's plenty of room for the buttons.
 3. This is my first PCB design ever. If you're good at this board and think, "well, that was a dumb decision" -- you're probably right! Feel free to let me know what I could do to improve the board. I would love for future versions to be as good as they can be!

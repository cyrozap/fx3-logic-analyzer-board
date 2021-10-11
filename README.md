# FX3 Logic Analyzer Board


## Introduction

This is a simple expansion board for the [Cypress FX3 SuperSpeed Explorer Kit (CYUSB3KIT-003)][kit] that turns it into a 16-channel, 100 MSps logic analyzer.


### Features

 - 16 input channels.
 - 100 MSps maxumim sample rate.
 - Supports logic levels of 1V8 and higher.
 - 5V tolerant inputs.
 - Connector pinout compatible with the [Digilent Analog Discovery][analog-discovery] and the [Analog Devices ADALM2000][adalm2000].
   - Cables can be purchased [here][cable], but the pin header has a standard 0.1 inch (2.54 mm) pitch, so any 0.1 inch pitch "dupont wire"/breadboard jumper wires will work.
 - Design suitable for manufacturing with budget/hobbyist PCB services.
   - 2 layers
   - 8-mil (0.2032 mm) minimum trace/space
   - 8-mil (0.2032 mm) minimum annular ring
   - 12-mil (0.3048 mm) minimum drill


## Images

[![A render of the front side of the PCB.][render-front]][render-front]
[![A render of the back side of the PCB.][render-back]][render-back]


## Errata


### v0.1

 - While the current design works, the return paths for the signal traces could use some improvement.
   Specifically, there should be ground paths routed either alongside or below each of the signal paths.
 - The input connector pinout should be labeled on the silkscreen.
 - The FX3 dev kit is a really tight fit, so the pin headers likely need to be moved a little closer together.
 - There currently isn't any kind of termination on the inputs, so sometimes for very fast signals the logic analyzer probe wires end up acting like stub wires and degrade the signal to the point that the Device Under Test (DUT) doesn't work properly.


## License

This project is released under the [Creative Commons Zero Public Domain Dedication][cc0], so please feel free to use or modify it however you like.


[kit]: https://www.cypress.com/documentation/development-kitsboards/cyusb3kit-003-ez-usb-fx3-superspeed-explorer-kit
[analog-discovery]: https://digilent.com/reference/test-and-measurement/analog-discovery/reference-manual#pin_out_diagram
[adalm2000]: https://wiki.analog.com/university/tools/m2k/devs/intro#pinout
[cable]: https://digilent.com/shop/2x15-flywires-signal-cable-assembly-for-the-analog-discovery/
[render-front]: doc/pcb-render-v0.1-front.png
[render-back]: doc/pcb-render-v0.1-back.png
[cc0]: https://creativecommons.org/publicdomain/zero/1.0/

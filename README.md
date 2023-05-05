# Pico W Enviro+ Pack sample
This is the [MicroPython](https://micropython.org) code that I'm running on the [Pico Enviro+ Pack from Pimoroni](https://shop.pimoroni.com/products/pico-enviro-pack).

- requires Pimoroni's [pirate-branded MicroPython for Pico](https://github.com/pimoroni/pimoroni-pico) 🏴‍☠️️

My Enviro+ sits on top of a Pico W. I wanted it to show the text display of the current environmental parameters, and also to publish the information to my MQTT broker at the same time. The [sample code from Pimoroni](https://github.com/pimoroni/pimoroni-pico/tree/main/micropython/examples/pico_enviro) is either/or, so, this repository contains an unholy mashup of a couple of chunks of their code, until I get around to doing something better.

Rather than using the full Enviro self-provisioning code for the standalone products, this is using a lightly-modified version of the `network_manager` code from Pimoroni as well.

In addition, I thought I'd noodle around with using the vector-ish Hershey fonts instead of using the bitmap ones, which gave me a chance to tinker with [PicoGraphics](https://github.com/pimoroni/pimoroni-pico/tree/main/micropython/modules/picographics). I'm happy with the result!

- open `config.py.example` in Thonny to add your wifi details (and save it as `config.py` when you're done). You'll also need to add MQTT details in there.
- for MQTT, you'll need to install `micropython-mqtt.simple` using Thonny's 'Tools' > 'Manage Packages' (or using `mip` - to be documented)
- transfer `config.py`, `main.py`, `network_manager.py` and the `lib` directory to your Pico.

Tested / running on MicroPython 1.20[.1] 👍🏻️

Now if you'll excuse me, I'm off to design 3D printed cases for Pimoroni products...

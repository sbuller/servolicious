![PCB](servolicious.jpg)

An eight port servo controller. Supply +5V, clock and data. 3v3 out from a uC looks good enough for the shift register.

Servo control is generally pulse widths of ~1500us, produced at 50Hz.
For 5us resolution the clock frequency will need to be 8bits * chain length * 200kHz.
Or 2MHz * chain length. The linked datasheet suggests 100MHz is viable, but the
board to board wiring may become a problem before that. Intercalating additional
grounds in the wiring may be required.

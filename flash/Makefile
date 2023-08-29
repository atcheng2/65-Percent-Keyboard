PORT = -P /dev/ttyUSB0
DEV = -p atmega32
BAUD = -b 19200

.PHONY: check
check:
	sudo avrdude -c avrisp $(DEV) $(BAUD) $(PORT)

.PHONY: fuse
fuse:
	sudo avrdude -c avrisp $(DEV) $(PORT) $(BAUD) -U lfuse:w:0x1F:m
	sudo avrdude -c avrisp $(DEV) $(PORT) $(BAUD) -U hfuse:w:0xC0:m

.PHONY: flash
flash:
	sudo avrdude -c avrisp $(DEV) $(PORT) $(BAUD) -U flash:w:main.hex:i

.PHONY: upload
upload:
	sudo avrdude -c usbasp $(DEV) $(PORT) $(BAUD) -U flash:w:andyboard_default.hex


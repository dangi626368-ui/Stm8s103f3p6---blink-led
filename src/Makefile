TARGET = main
CC = sdcc
PACK = packihx

all: $(TARGET).hex

$(TARGET).ihx: src/main.c
	$(CC) --model stm8 --out-fmt-ihx src/main.c -o $(TARGET).ihx

$(TARGET).hex: $(TARGET).ihx
	$(PACK) $(TARGET).ihx > $(TARGET).hex

clean:
	rm -f $(TARGET).ihx $(TARGET).hex *.rel *.sym *.lk

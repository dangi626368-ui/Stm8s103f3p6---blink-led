#include "stm8s.h"

void delay_ms(uint16_t ms) {
    uint16_t i, j;
    for (i = 0; i < ms; i++) {
        for (j = 0; j < 1200; j++) {
            __asm__("nop");
        }
    }
}

void main(void) {
    // On-board LED = PC5
    GPIOC->DDR |= (1 << 5);
    GPIOC->CR1 |= (1 << 5);
    GPIOC->CR2 &= ~(1 << 5);

    while (1) {
        GPIOC->ODR ^= (1 << 5);
        delay_ms(500);
    }
}

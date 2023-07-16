Hardware setup for polling button and turning on LED when button is pressed and
reading IRQ from button and toggling LED when button is pressed.

		VCC
		|
		|-----------------------|
		|			|
	       SW1		       R1/1k					led_poll    led_irq
		|			|					   |		|
button_poll-----|			|-------R1/1k------|			 D1/led	     D2/led
		|			|		   |			   |		|
		|			|		   |-----button_irq	   |		|
		|			|		   |			   |		|
	       R1/1k		       SW2		  C1/1uF		 R2/220	     R2/220
		|			|		   |			   |		|
		|			|		   |			   |		|
		|-----------------------------|-------------------------------------------------|
					      |
					     GND

button_poll/button_irq/led_poll/led_irq are pins on the microcontroller.
R# are resistors, C# are capacitors, D# are LEDs, SW# are switches.

LCD-Keypad Multiplexed Interfacing
==================================

Using a Keypad along with an LCD Display often eats up the I/O pins on the micro-controller. The solution reduce the number of pins needed to interface both is, multiplex the data bus.

*Function calls for Keypad when multiplexed with LCD

Use this function if you want to wait for a key
Key = Keypad_ALTwaitForKey();    // Waits until a key is pressed

Use this instead of above function if you don't want to wait
Key = Keypad_ALTgetKey();    // It gets the Key or return 0

You must to define the multiplexed pins in both lcd.h and Keypad.h

//Pin defines for HD44780 based Character LCD
// Data bus for 4 bit mode
//#define LCD_4			RB4
//#define LCD_5			RB5
//#define LCD_6			RB6
//#define LCD_7			RB7

// TRIS Setting for a pins
//#define LCD_4_dir		TRISB4
//#define LCD_5_dir		TRISB5
//#define LCD_6_dir		TRISB6
//#define LCD_7_dir		TRISB7


// Pin defines for Keypad
//connect to the column pinouts of the keypad
//#define KP_COL1			RB4
//#define KP_COL2			RB5
//#define KP_COL3			RB6
//#define KP_COL4			RB7

//Direction control
//#define KP_COL1_dir             TRISB4
//#define KP_COL2_dir             TRISB5
//#define KP_COL3_dir             TRISB6
//#define KP_COL4_dir             TRISB7

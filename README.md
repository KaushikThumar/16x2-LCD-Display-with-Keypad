# 16x2-LCD-Display-with-Keypad
In Embedded system design, matrix keypad (4x4, 4x3, 3x3 or 5x5) is used for key in the user inputs. Similarly character LCD display [16x2, 16x4, 20x2 or 20x4 LCDs] is used for indicating the system status / parameters. 

# Parts and components
Arduino Uno board
16x2 LCD
1 K ohm potentiometer
4x4 matrix keypad

![image](https://user-images.githubusercontent.com/92664692/138494265-e3c4c795-e2ec-41c0-bdc9-33f87632d55b.png)

The 16x2 is very common type LCD, with two rows, and each row displays 16 characters of either 5x7 or 5x8 dot matrix characters. The LCD is available in a 16 pin package. It consists of back light and contrast adjustment function and each dot matrix has 5×8 dot resolution. The 16x2 LCD display is connected to the Arduino (A0,A1,A2,A3,A4,A5) analog IO pins, where those pins are configured as digital in / out, where LCD operates at 4 bit data mode. If the display is not visible, adjust the Contrast pot (1K), to make it visible.

Matrix key pad is arranged by push button switches in rows and columns.In a simple technique, the 16 keys of matrix keypad is connected with 8 digital IO pins of Arduino. Usually the keypad scan procedure is The key is decoded through Column selection / Row read. Write HIGH to Column One. And keep rest of the Column to LOW. Scan (Read) the Row One to Row Four, to find the key. Repeat until a key press (are multiple) is identified. The Row pins are connected to 5,4,3 and 2nd digital IO pins of Arduino. The Column pins are connected to 6,7,8 and 9th digital IO pins of Arduino. The Arduino LiquidCrystal and Keypad library is used for displaying the status and detecting key press.

# New-Holland-Headland-Turn-Sequence-Button-board
Small PCB to create a transistor switch triggered by pressing the headland turn sequence button on a New Holland Tractor with a classic armrest

This PCB makes it possible to use the headland turn sequence button on the New Holland multifunction handle on the classic armrest to activate auto steer on my AgOpenGPS board.

On the classic armrest tractors, the buttons are purely analogue. The central control unit (CCU) supplies 5v and there is a voltage divider circuit so that the signal wire has roughly 1.5v when the button is not pressed, rising to roughly 3.5v when the button is pressed. The CCU detects this voltage change and acts accordingly.

This board utilises the voltage change to drive a transistor switch effectively operating like the momentary button I previously used to engage the autosteer. Because I've found my muscle memory keeps kicking in, I also retain the existing switch, which sits in parallel to the transistor switch, meaning I can operate either via the headland turn sequence button or via my existing button.

The AgOpenGPS boards I use (All-In-One v4.5 and a Kaupoimod pcb v4) use a button switch to complete the circuit from an optocoupler to ground, allowing the board to recognise the press of the switch. The positive voltage output from the board has to be connected to V+ terminal and the ground to the GND terminal to allow the transistor to work.

<img width="595" height="396" alt="Circuit board" src="https://github.com/user-attachments/assets/2a7496ca-50f5-4e93-a149-bd77f4bfed5d" />

So I could work non-destructively, I built a small wiring loom to sit between the FCI/SCIMA 24 pin plug that joins the armrest harnes to the CCU harness. On this, the HTS signal button is pin C6 and I just take a splice off this to the transistor switch.
. Make sure you don't accidentally buy the wrong colour plugs though, as this meant I had to cut the incorrect keying off to fit!
<img width="1582" height="1659" alt="20261020_112808 (cropped)" src="https://github.com/user-attachments/assets/1fab8ff1-8b1c-4dc1-80dd-9e25ece97dd3" />

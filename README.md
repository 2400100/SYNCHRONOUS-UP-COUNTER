### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.


**PROCEDURE**

1.Initialize the shift register to a known state (e.g., all zeros).

2.Input a bit serially into the shift register.

3.Shift the contents of the register one position to the right (or left).

4.Output the shifted bit from the last stage of the register.

5.Repeat steps 2-4 for each bit you want to input and shift.

**PROGRAM**


![Screenshot 2024-12-20 142700](https://github.com/user-attachments/assets/c7228071-6f8c-47d2-97a8-6ecffea695fe)


Developed by: SUBIKSHA K RegisterNumber: 2400100

**RTL LOGIC UP COUNTER**


![Screenshot 2024-12-20 142717](https://github.com/user-attachments/assets/c418069b-06fa-4515-b51f-720614bb41d5)


**TIMING DIAGRAM FOR IP COUNTER**


![Screenshot 2025-01-02 213957](https://github.com/user-attachments/assets/117f867a-3001-4c88-b201-e4921714185f)





**TRUTHTABLE**

![Screenshot 2025-01-02 214030](https://github.com/user-attachments/assets/7bd819dd-80b3-4fbc-9709-f035c576daff)



**RESULTS**

 SYNCHRONOUS-UP-COUNTER has been studied and verified successfully using quartus software.

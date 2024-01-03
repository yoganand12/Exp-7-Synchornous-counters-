## Exp:6 Synchornous counters up counter and down counter 
### AIM: To implement 3 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  
PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:  
Quartus prime
### THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.
Note that each bit in this 3-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.
Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.
The Q outputs of each flip-flop will serve as the respective binary bits of the final, 3-bit count:
Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)
## DOWN COUNTER 
As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.
This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.

![Screenshot 2024-01-03 222836](https://github.com/yoganand12/Exp-7-Synchornous-counters-/assets/155515519/e075cff9-1fe4-4029-b129-2e19922533eb)

3-bit Count Down Counter
### PROGRAM 

## UP COUNTER 

![Screenshot 2024-01-03 222338](https://github.com/yoganand12/Exp-7-Synchornous-counters-/assets/155515519/2368914b-51be-4ede-87a1-9113b31ebaa9)

## DOWN COUNTER 

![Screenshot 2024-01-03 222344](https://github.com/yoganand12/Exp-7-Synchornous-counters-/assets/155515519/8bca5215-6212-424a-a4b2-c566962b1756)

Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: 
### RTL LOGIC

## UP COUNTER 

![Screenshot 2024-01-03 222355](https://github.com/yoganand12/Exp-7-Synchornous-counters-/assets/155515519/77763d1d-14a1-4a49-8c3d-48f62e6ceae0)


## DOWN COUNTER  

![Screenshot 2024-01-03 222403](https://github.com/yoganand12/Exp-7-Synchornous-counters-/assets/155515519/f8f9e5d9-3949-4063-8d06-049b94629405)

### TIMING DIGRAMS FOR COUNTER  

## UP COUNTER 
![Screenshot 2024-01-03 222410](https://github.com/yoganand12/Exp-7-Synchornous-counters-/assets/155515519/04800bf7-fd6c-4b77-9f9f-1ead12817117)


## DOWN COUNTER  
![Screenshot 2024-01-03 222417](https://github.com/yoganand12/Exp-7-Synchornous-counters-/assets/155515519/36607b55-fb8e-4fed-87db-0cc65d2d26f7)

### TRUTH TABLE 

## UP COUNTER 
![Screenshot 2024-01-03 222620](https://github.com/yoganand12/Exp-7-Synchornous-counters-/assets/155515519/f3bde57a-f552-4083-998d-09a8eeb0b5df)


## DOWN COUNTER  
![Screenshot 2024-01-03 222628](https://github.com/yoganand12/Exp-7-Synchornous-counters-/assets/155515519/d43be26f-58ff-4c7c-9d16-d035915401ae)


### RESULTS:

![Screenshot 2024-01-03 222641](https://github.com/yoganand12/Exp-7-Synchornous-counters-/assets/155515519/153a3c61-db2f-4efe-ada9-82b009ad9ed3)


Developed by: JAYANI N

RegisterNumber: 212224100025


# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**



**PROGRAM**

      module DE2 (
          input clk,
          input serial_in,
          output serial_out
      );
      
          reg q0, q1, q2, q3;
      
          always @(posedge clk) begin
              q3 <= q2;
              q2 <= q1;
              q1 <= q0;
              q0 <= serial_in;
          end
      
          assign serial_out = q3;
      
      endmodule

**RTL LOGIC FOR SISO Shift Register**
![image](https://github.com/user-attachments/assets/f76f8b64-faf4-4d21-924d-cc54111e3dbd)


**TRUTH TABLE**
![image](https://github.com/user-attachments/assets/1c2ab47e-040c-4b27-b691-8652cd94c374)



**TIMING DIGRAMS FOR SISO Shift Register**
![image](https://github.com/user-attachments/assets/22c35026-c44e-4107-9439-c771f8b44886)


**RESULTS**
Thus, the simulation has been verified using quartus.

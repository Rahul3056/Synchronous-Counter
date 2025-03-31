### **Synchronous Counter**  

#### **Concept Overview**  
A **Synchronous Counter** is a type of counter where all flip-flops are triggered by the same clock signal simultaneously. Unlike an **asynchronous counter**, there is **no ripple delay** because all flip-flops change state at the same time.  

#### **Detailed Explanation**  
- Uses **JK or T flip-flops** connected in parallel.  
- The clock signal is **applied to all flip-flops simultaneously**, ensuring fast and glitch-free operation.  
- The **toggle condition** for each flip-flop is determined by logic gates, which ensure that each stage changes only when required.  
- **Advantages:** Faster operation, no ripple delay, and better synchronization compared to asynchronous counters.  

#### **Example: 3-bit Synchronous Counter (MOD-8 Counter)**  
- **Uses 3 JK flip-flops**, toggling based on logic conditions.  
- **Counts from 000 to 111 (0 to 7 in decimal) and resets to 000**.  

#### **Truth Table (MOD-8 Counter)**  

| Clock | Q2 | Q1 | Q0 | Decimal |  
|-------|----|----|----|---------|  
| 0     | 0  | 0  | 0  | 0       |  
| 1     | 0  | 0  | 1  | 1       |  
| 2     | 0  | 1  | 0  | 2       |  
| 3     | 0  | 1  | 1  | 3       |  
| 4     | 1  | 0  | 0  | 4       |  
| 5     | 1  | 0  | 1  | 5       |  
| 6     | 1  | 1  | 0  | 6       |  
| 7     | 1  | 1  | 1  | 7       |  
| 8     | 0  | 0  | 0  | 0 (Reset) |  

#### **Boolean Expressions**  
- `Q0 toggles on every clock pulse`  
- `Q1 toggles when Q0 = 1`  
- `Q2 toggles when Q0 = 1 and Q1 = 1`  

#### **Applications**  
Used in **high-speed counting applications, digital clocks, frequency counters, and synchronous circuits**.  

#### **Execution Steps**  
1. Open **QuestaSim, ModelSim, Xilinx ISE, or Vivado**.  
2. Write the **Verilog code** for a 3-bit synchronous counter.  
3. Create a **testbench** to simulate the counter operation.  
4. Check the **waveform output** to verify the counting sequence.  

#### **Real-World Example for Practice**  
Design a **4-bit Synchronous Counter (MOD-16)** using **4 JK flip-flops**.  `

#### **Further Enhancements**  
- Implement a **4-bit Synchronous Counter (MOD-16)**.  
- Add an **active-low Reset** to restart counting when needed.  

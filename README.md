# CMOS-XOR-Gate-Design-using-Cadence-Virtuoso
### 2-input CMOS XOR Gate Design and Analysis with Layout using Cadence Virtuoso

---
<!-- Cadence Project (Transient, DC, AC & Noise Response With Layout) -->

I’m really glad to share that, this is my fifth project on __Cadence Virtuoso__. I am designing here a 2-input CMOS XOR Gate Design by 4 CMOS NAND Gate, with it's Layout using Cadence Virtuoso.

___Before I start explaining my project in details, you should know a few things !___     

### What is CMOS XOR Gate?  
CMOS XOR Gate (sometimes EOR or EXOR and pronounced as Exclusive OR) is a digital logic gate that gives a true (1/HIGH) output when the number of true inputs is odd. An XOR gate implements an exclusive from mathematical logic; that is, a true output results if one, and only one, of the inputs to the gate is true. If both inputs are false (0/LOW) or both are true, a false output results. XOR represents the inequality function, i.e., the output is true if the inputs are not alike otherwise the output is false. A way to remember XOR is "must have one or the other but not both".

XOR can also be viewed as addition modulo 2. As a result, XOR gates are used to implement binary addition in computers. A half adder consists of an XOR gate and an AND gate. Other uses include subtractors, comparators, and controlled inverters.

### The Project details of mine :
Here i have use __gpdk90n__ :-
1. 5T pmos1v and 5T nmos1v.
2. For vdd i have use vdc (1.2v)
3. For input i have use two vpulse (1.2v)
4. Here I am doing four types of Analysis :  
    i ) Transient Response  
    ii ) DC Response  
    iii ) AC Response  
    iv ) Noise Response  
    N.B. I'm Calculated the Power Consumption (Average Power) of this circuit using Calculator.
5. In Layout - Metals Used ( Metal1, Metal2 & Poly for gate )
6. The minimum width of metal utilized for routing is 0.12
7. DRC and LVS clean (there are no error)

So I designed a Schematic of the CMOS XOR Gate, where the whole thing is based on gpdk90n. I have use 8 pmos for 1v and 8 nmos for 1v. I also designed a symbol of it, so that i can utilise that for further schematic creation.  

The below figure shows a 2-input CMOS XOR Gate. For Designing a XOR Gate i have use to 4 NAND Gate.

Considering all steps will show that Vout is following the expected value as in 2-input XOR Gate Truth Table.

![Scametic](https://github.com/wreasin/CMOS-XOR-Gate-Design-using-Cadence-Virtuoso/blob/main/image/Scametic.PNG?raw=true)

#### Transient, DC, AC & Noise Response :
_Here I am doing four types of Analysis - DC, AC, Transient and Noise_.  
In DC and Transient Analysis i have measured Va, Vb & Vout as Voltage, and Current (I) in VDD node. In AC Analysis i have measured Va, Vb & Vout as Voltage Frequency and Current (I) Frequency in VDD node. For DC and Transient Analysis the plots of _Va_ , _Vb_ and _Vout_ shows the _voltages_, on the otherhand _VDD(I4)_ shows the _current (I)_. For AC Analysis the plots of _Va_ , _Vb_ and _Vout_ shows the _voltage frequency_, on the otherhand _VDD(I4)_ shows the _current (I) frequency_. For measuring of Noise Figure and Noise Response i had to use PORTS instead of Vpulse. For Noise Analysis i have measured input, output & VN2 noise and also Noise Figure. In Noise Response the plots shows the input, output & VN2 noise and also Noise Figure. 
![Symbol_Scametic](https://github.com/wreasin/CMOS-XOR-Gate-Design-using-Cadence-Virtuoso/blob/main/image/Symbol%20%26%20For%20Analysis.PNG)  
![output](https://github.com/wreasin/CMOS-XOR-Gate-Design-using-Cadence-Virtuoso/blob/main/image/Tran%20AC%20DC%20Noise%20Analysis.PNG)  

#### Calculating Power Consumption of this circuit using Calculator:  
Calculating Power Consumption Calculator for CMOS XOR Gate. The calculator allows you to calculate both the total power consumption of the circuit. By inputting relevant parameters, I've determine the power requirements of the circuit, aiding in design and optimization processes.  
![Power Consumption on ADE L](https://github.com/wreasin/CMOS-XOR-Gate-Design-using-Cadence-Virtuoso/blob/main/image/Power_Consumption%20on%20ADE%20L.PNG)
![Power Consumption using Calculator](https://github.com/wreasin/CMOS-XOR-Gate-Design-using-Cadence-Virtuoso/blob/main/image/Power_Consumption%20using%20Calculator.PNG)

#### Layout :
In Layout i have use  Metal1 and Poly Layer. I have use here X & Y snap spacing is 0.005m and also the minimum width of metal utilized for routing is 0.12.  
![Layout](https://github.com/wreasin/CMOS-XOR-Gate-Design-using-Cadence-Virtuoso/blob/main/image/Layout.PNG)

#### Design Rule Check (DRC)  
DRC is clean. There are no error in DRC.  
![DRC](https://github.com/wreasin/CMOS-XOR-Gate-Design-using-Cadence-Virtuoso/blob/main/image/DRC%20Check.PNG)  

#### Layout Versus Schematic (LVS)  
LVS is clean. There are no error in LVS.  
![LVS](https://github.com/wreasin/CMOS-XOR-Gate-Design-using-Cadence-Virtuoso/blob/main/image/LVS%20Check.PNG)

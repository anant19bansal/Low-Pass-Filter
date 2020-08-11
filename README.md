# Low-Pass-FIR-Filter
Designed and simulated a 31-tap Low Pass FIR Digital Filter using Verilog which takes 8-bit input samples.
### Specifications
  - Design technique   - Window based FIR filter design
  - Cutoff frequency   - 3kHz
  - Sampling frequency - 48kHz
### Description
Finite impulse response (FIR) filters are filters whose impulse response (or response to any finite length input) is of finite duration, because it settles to zero in finite time.
These filters do not use feedback and their output is only related to current and previous inputs. <br>
A causal discrete-time FIR filter of order N has the output sequence as the weighted sum of previous input values:
<img src = ""><br>
#### where:
  - x[n] is the input signal
  - y[n] is the output signal
  - N is the filter order
  - bi is the filter coefficient
  <br>
  
  <img src = ""><br>
  The following MATLAB command was used to calculate the coefficients:<br><br>
  ```a = round(fir1(30,0.125)*1024)```<br><br>
  Usually filter coefficients are real numbers in the range [-1,1] but realistically we can only build hardware to do integer arithmetic. So the coefficients have been scaled i.e multiplied by 1024 and rounded to integers.

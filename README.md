# HuggingFive :raised_hand_with_fingers_splayed:
HuggingFive :raised_hand_with_fingers_splayed: is a collection of ML functions and libraries written in RISC-V assembly and C. This includes neural network layers, activation functions, as well as entire neural networks. Think of it as a low-level HuggingFace for RISC-V assembly code.  The hope is to eventually roll all these handwritten tricks into the existing compiler toolchains (or have AI generate even better assembly code). 

<table>
  <tr>
    <th rowspan="2"><b>Description</b></td>
    <th rowspan="2"><b>Author</b></td>
    <th rowspan="2"><b>RV config</b></td>
    <th rowspan="2"><b>Data types</b></td>
    <th colspan="4"><b>Performance numbers for an exemplary config</b></td>
    <th rowspan="2"><b>Notes</b></td>
  </tr> <tr>
    <th><b>Config</b></td>
    <th><b>Ops</b></td>
    <th><b>Register utilization</b></td>
    <th><b>Memory size (B)</b></td>   
  </tr> <tr>
    <!--- Conv2D 1x1 --->
    <td><a href='https://github.com/OpenMachine-ai/tinyfive/blob/main/layer_examples.py'>Conv2D 1x1</a></td>
    <td>OpenMachine</td>
    <td>RV32IF</td>
    <td>FP32</td>
    <td>C=32, F=32, R=6x6</td>
    <td>57,953</td>
    <td>8/31 x-regs; 21/32 f-regs</td>
    <td></td>
    <td></td>
  </tr> <tr>
    <!--- add your entry here --->
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</table>
<!--- Note: use HTML for the table above because markdown doesn't support cell-merging --->

- C : input channels
- F : output channels (or filters), only used if F is not the same as C
- R : input resolution
- Q : output resolution, only used if Q is not the same as R
  


## Contributing
Please add your functions and routines to HuggingFive :raised_hand_with_fingers_splayed:: Add a link to your function in the 
table and submit a PR, which will get approved promptly because there are no rules here.


More details coming soon ...

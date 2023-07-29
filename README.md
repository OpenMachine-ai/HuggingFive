# HuggingFive :raised_hand_with_fingers_splayed:
HuggingFive :raised_hand_with_fingers_splayed: is a collection of ML functions and libraries written in RISC-V assembly and C.  This includes neural network layers, activation functions, as well as entire neural networks. Think of it as a low-level HuggingFace for RISC-V assembly code.  The table below includes performance numbers for benchmarking.  The hope is to eventually roll all these handwritten tricks into the existing compiler toolchains (or have AI generate even better assembly code). 

<table>
  <tr>
    <th rowspan="2">Description</td>
    <th rowspan="2">Author</td>
    <th rowspan="2">RV config</td>
    <th rowspan="2">Data types</td>
    <th colspan="5">Performance numbers for an exemplary config</td>
    <th rowspan="2">Notes</td>
  </tr> <tr>
    <th>Config</td>
    <th>MACs</td>
    <th>Ops</td>
    <th><b>Register utilization</b></td>
    <th><b>Memory size (B)</b></td>   
  </tr> <tr>
    <!--- Conv2D 1x1 --->
    <td><a href='https://github.com/OpenMachine-ai/tinyfive/blob/main/layer_examples.py'>Conv2D 1x1</a></td>
    <td>OpenMachine</td>
    <td>RV32IF</td>
    <td>FP32</td>
    <td>C=32, F=32, R=6</td>
    <td>C F R<sup>2</sup> = 36,864</td>
    <td>57,953</td>
    <td>8/31 x-regs, 21/32 f-regs</td>
    <td></td>
    <td></td>
  </tr> <tr>
    <!--- Conv2D 3x3 --->
    <td><a href='https://github.com/OpenMachine-ai/tinyfive/blob/main/layer_examples.py'>Conv2D 3x3</a></td>
    <td>OpenMachine</td>
    <td>RV32IF</td>
    <td>FP32</td>
    <td>C=3, F=8, R=12, stride=1</td>
    <td>9 C F R<sup>2</sup> = 31,104</td>
    <td>TBD</td>
    <td>TBD</td>
    <td></td>
    <td></td>
  </tr> <tr>
    <!--- Depthwise Conv2D 3x3 --->
    <td><a href='https://github.com/OpenMachine-ai/tinyfive/blob/main/layer_examples.py'>Depthwise Conv2D 3x3</a></td>
    <td>OpenMachine</td>
    <td>RV32IF</td>
    <td>FP32</td>
    <td>C=4, R=6, stride=1</td>
    <td> 9 C R<sup>2</sup> = 1,296</td>
    <td>TBD</td>
    <td>TBD</td>
    <td></td>
    <td></td>
  </tr> <tr>
    <!--- please add your entry here --->
    <td></td>
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
- R : square root of input resolution (e.g. R=6 for image resolution of 6x6 pixels)
- Q : square root of output resolution, only used if Q is not the same as R
- MACs : number of fused multiply-accumulate operations required by the neural-network layer (can be used as a lower-bound for total number of ops; this number ignores possible savings from zero-padding for conv-layers)  


## Contribute
Please add your functions and routines to HuggingFive :raised_hand_with_fingers_splayed:: Add a link to your code in the 
table and submit a PR, which will get approved promptly because there are no rules here.


More details coming soon ...

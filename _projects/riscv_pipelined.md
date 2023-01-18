---
layout: page
title: Pipelined RISC-V processor
description: 5-stage pipelined RISC-V processor with instruction cache and data cache
img: assets/img/riscv.png
github: https://github.com/Alexsung929/RISCV-Pipeline-Project
importance: 1
category: Course Work
---
## Usuage 
Copy content in the files below into CHIP.v, and run ...
1. $ncverilog Final_tb.v CHIP.v slow_memory.v +define+hasHazard +access+r
2. $ncverilog Final_tb.v CHIP.v slow_memory.v +define+BrPred +access+r
3. $ncverilog Final_tb.v CHIP.v slow_memory.v +define+compression +access+r 

## BaseLine
  CHIP_hasHazard.v
  
## Extension:

* BrPred:
  1. 2-bits predictor: CHIP_Bred.v
  2. 2-bits predictor(小改）:  CHIP_Bred_comp2.v 
  3. without prediction: CHIP_Bred_comp1.v (from baseline)

* Compress: 
  CHIP_compress.v

* L2_cache:
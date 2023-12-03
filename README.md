WORK IN PROGRESS

# Building + Testing on Pocket Hardware

[agg23](https://github.com/agg23/analogue-pocket-utils/wiki/Getting-Started) has very kindly shared their Analogue Pocket development experience to make this project possible. 

To build a bitstream for the Pocket, open the `Pocket.qpf` project file. It is configured to look for the PipelineC output Quartus IP `.qip` file `/vhdl/pipelinec_top.qip`. Click Generate Bitstream. Upload the bitstream to the Pocket. For more information see [tutorials for using Quartus](https://github.com/agg23/analogue-pocket-utils/wiki/Quartus).

Note that the `pipelinec_top.qip` `top` module requires the following inputs 
```vhdl
TODO list IO ports for top ports
include dumb loopback of frame clock needed for quartus work around
```

# CflexHDL + PipelineC Flow

The above mentioned `/vhdl/pipelinec_top.qip` file and other associated outputs in `vhdl/` are the output of the [CflexhHDL](https://github.com/suarezvictor/CflexHDL) and [PipelineC](https://github.com/JulianKemmerer/PipelineC) based flow documented [here](https://github.com/JulianKemmerer/PipelineC-Graphics).

Build the project using the `make` based flow, ex.
`make BOARD=pocket`. CflexHDL code generation runs first producing PipelineC. Which is followed by many synthesis+PnR runs for PipelineC autopipelining to produce VHDL.

# Chasing the Beam Graphics

Explain how the pattern gen works in C code, and how more advanced graphics need more complex rendering pipeline.

Is it possible to also show the donut demo too?


# Sphery vs. Shapes Partial Demo

Show folks what we have working so far with RT_SMALL_UI, explain the issue of device resources, explain some ideas we might have (fast clocks and iterations), call for help etc.

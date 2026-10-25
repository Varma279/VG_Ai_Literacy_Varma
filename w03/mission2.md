# OpenROAD: Open-Source VLSI Tool Investigation

## 1. Introduction

ASIC physical design transforms a synthesized digital circuit into a physical implementation that can be manufactured. This process involves several stages, including floorplanning, placement, clock-tree synthesis, routing, and timing analysis.

OpenROAD is an open-source project that provides tools for automating important parts of digital chip implementation. Investigating it helps me understand how open-source software can be used to explore physical-design workflows.

**Official resources:**
- [OpenROAD Documentation](https://openroad.readthedocs.io/en/latest/)
- [OpenROAD GitHub Repository](https://github.com/The-OpenROAD-Project/OpenROAD)
- [OpenROAD-flow-scripts](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts)

## 2. Purpose and Capabilities

| Aspect | Description |
|---|---|
| Main purpose | Support automated digital ASIC implementation and physical-design tasks. |
| Design input | Depends on the workflow; commonly includes a synthesized netlist and technology-related files. |
| Technology information | Liberty timing libraries, LEF physical abstracts, and other technology files required by the selected flow. |
| Design constraints | Timing and design constraints supplied through supported constraint files, such as SDC. |
| Physical-design activities | Floorplanning, placement, clock-tree synthesis, routing, and related optimisation steps. |
| Possible outputs | Updated design databases, implementation files, reports, and other outputs depending on the flow and configuration. |

The precise inputs and outputs depend on the chosen platform, configuration, and implementation stage.

## 3. Where OpenROAD Fits in the Design Flow

A typical digital ASIC implementation flow can be represented as follows:

1. **RTL design:** Describe the circuit using a hardware description language such as Verilog.
2. **Logic synthesis:** Use a synthesis tool such as Yosys to convert RTL into a gate-level netlist.
3. **Floorplanning:** Define the chip or block dimensions and establish the initial physical layout.
4. **Placement:** Position standard cells within the available layout area.
5. **Clock-tree synthesis:** Build the clock distribution network for sequential elements.
6. **Routing:** Create physical connections between cells and other design components.
7. **Timing and design checks:** Examine timing reports and physical-design violations.
8. **Final outputs:** Generate the required implementation files and reports for the selected flow.

This is a simplified overview. Actual flows may include additional preparation, optimisation, verification, and sign-off stages.

## 4. Important Inputs and Outputs

| File or Data Type | Role in the Workflow |
|---|---|
| Verilog RTL | Describes the digital circuit before synthesis. |
| Gate-level netlist | Represents the circuit using synthesised logic cells. |
| Liberty (`.lib`) | Provides cell characteristics, including timing and power information. |
| LEF (`.lef`) | Describes physical information about technology and cell layouts. |
| SDC (`.sdc`) | Specifies timing constraints such as clocks and input/output delays. |
| DEF (`.def`) | Represents physical-design information such as component placement and routing. |
| Reports | Summarise results such as timing, area, and design-rule checks. |

Not every stage requires every file listed above. Requirements depend on the selected platform and flow.

## 5. Potential Applications of AI and Machine Learning

Machine learning could support certain physical-design tasks by analysing design data, identifying patterns, or estimating results. These are possible applications rather than claims that every capability is already implemented in OpenROAD.

| Engineering Task | Potential AI/ML Contribution |
|---|---|
| Placement optimisation | Estimate the impact of different placement choices on wirelength or congestion. |
| Timing analysis | Predict potential timing problems from design features and previous results. |
| Congestion estimation | Identify regions that may experience routing difficulties. |
| Power estimation | Estimate power consumption using design characteristics and suitable training data. |
| Parameter tuning | Help explore configuration settings that may improve implementation results. |

Any model-generated recommendation would need to be evaluated against actual tool results and appropriate engineering constraints.

## 6. Practical Exploration

The following activities can be used to investigate OpenROAD using an existing installation or a suitable example project.

- Review the official documentation to understand the tool's purpose and supported workflow.
- Inspect an example project and identify its netlist, technology files, and timing constraints.
- Determine which implementation stage the example is intended to run.
- If the environment is available, attempt to run a small example using its documented instructions.
- Examine the generated reports and identify metrics such as cell area, timing, and routing-related results.

**My experiment record**

- **Environment used:** To be filled in.
- **Example or design explored:** To be filled in.
- **Steps completed:** To be filled in.
- **Results or errors observed:** To be filled in.
- **What I learned:** To be filled in.

These fields should reflect the work actually performed. Reading documentation alone should not be reported as successfully running a design.

## 7. Challenges and Further Learning

Areas that may require additional study include understanding technology libraries, preparing valid timing constraints, interpreting timing reports, and resolving physical-design violations.

I also want to understand how changes in placement and routing affect power, performance, and area (PPA), and how data-driven methods could help engineers explore design choices more efficiently.

## 8. Conclusion

OpenROAD provides an opportunity to investigate digital ASIC implementation using open-source tools. Understanding its workflow and required input files is an important step toward learning physical design.

Combining practical tool exploration with reliable documentation and careful evaluation can also help identify where AI and machine learning may be useful in future engineering workflows.

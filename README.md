# Quick RISC-V Extension: loop_continue

## Overview

This project introduces a custom RISC-V instruction, loop_continue, designed to accelerate common loop patterns in Javascript, utilizing the embedded interpreter QuickJS.

The extension is implemented as a set of patches to the RISC-V toolchain and simulator, with supporting tests and documentation. By isolating the changes in this repo, the upstream toolchain (riscv-gnu-toolchain) and simulator (riscv-isa-sim) remain pristine.

## Features

- New instruction: loop_continue rs1, rs2
- Increments a loop index and checks against a loop limit.
- Simplifies loop control, reducing overhead in interpreter workloads.
- Patches: for both assembler/disassembler (binutils) and execution semantics (Spike).
- Tests: C, assembly, and JavaScript examples using the new instruction.
- Automation scripts: to apply patches, rebuild, and run tests in one step.
- Documentation: ISA encoding, design notes, and usage examples.
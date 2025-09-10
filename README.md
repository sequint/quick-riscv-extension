# Quick RISC-V Extension: ror (Rotate Right)

This project introduces a custom RISC-V instruction, ror (rotate right), designed as a lightweight extension to validate a RISC-V development workflow.

The extension is implemented as a set of patches for the RISC-V toolchain and simulator, along with assembly and C++ tests. The goal is to provide a minimal, reproducible extension that demonstrates the full path from instruction design → toolchain integration → simulator execution → test programs.

## Features

- New instruction: ror rd, rs1, rs2
    - Rotates the contents of rs1 right by the shift amount in rs2.
    - Bit rotation is not part of the base RISC-V ISA, making this an instructive custom addition.
- Patches: add assembler/disassembler support (binutils) and execution semantics (Spike).
- Tests:
    - Assembly program demonstrating ror.
    - C++ program using inline assembly with ror.
- Automation scripts: to apply patches, rebuild, and run tests.
- Documentation: ISA encoding, pseudocode, and design notes.
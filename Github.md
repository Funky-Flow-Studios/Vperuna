# Vperuna Engineering Environment

## Overview
This repository contains the **Vperuna** high-performance VPN orchestration engine, featuring:
- **Rust Core (`hp_dor_core`)**: AVX2-optimized SIMD data processing.
- **Node.js Orchestrator**: Agent-based system management.
- **Admin Tools**: Integrated Intel VTune, SDE, and Ghidra workflows.

## Quick Start (Engineering Mode)

1.  **Prerequisites**:
    - Windows 10/11 (Admin privileges required for profiling).
    - Rust (Cargo).
    - Node.js (npm).
    - Intel oneAPI Base Toolkit (VTune) - *Optional*.
    - Intel SDE - *Optional*.

2.  **Installation**:
    ```bash
    npm install
    ```

3.  **Full System Check & Build**:
    Run the automated engineering script (Administrator):
    ```cmd
    FULL_ADMIN_RUN_TOOLS.bat
    ```
    This script will:
    - Request Admin privileges.
    - Build the Rust core with AVX2 optimizations.
    - Run Unit Tests.
    - Execute Intel VTune Profiling (Hotspots).
    - Verify Instruction Mix with Intel SDE.
    - Perform Security Audit (Ghidra/SHA256).

4.  **Logs & Reports**:
    - Execution Log: `admin_agent_execution.log`
    - Profiling Data: `vtune_results/`
    - SDE Report: `sde_mix_report.out`

## Architecture
- `src/` - TypeScript Source
- `src/rust/` - Rust FFI Core
- `clean_release/` - Obfuscated Deployment Build

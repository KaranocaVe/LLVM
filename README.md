# LowLevelVpnMachine (LLVM)

**High-Performance, Cross-Platform Transparent Proxy Core powered by eBPF/C.**

-----

## Overview

LLVM (LowLevelVpnMachine) is an innovative networking core designed to implement a **high-performance, truly "unaware" (no TUN/TAP)** transparent proxy data plane directly within the operating system kernel.

It leverages the **eBPF (Extended Berkeley Packet Filter)** framework, programmed in **C/libbpf**, to overcome the performance bottlenecks of traditional virtual network interfaces, establishing a kernel-native proxy core.

> **Note:** LLVM stands for LowLevelVpnMachine and is not affiliated with the LLVM Compiler Infrastructure.

## Platform & Tech Stack

| Platform | Technology Stack | Status | Focus |
| :--- | :--- | :--- | :--- |
| **Linux** | C/libbpf (eBPF, XDP/TC) | **Core Support** | Kernel-native performance for data processing. |
| **Windows**| C/libbpf (eBPF for Windows / WFP) | *Roadmap* | Achieving bytecode compatibility and high performance on Windows. |

## Quick Start (Linux)

### Prerequisites

  * Linux Kernel 4.18+
  * Clang/LLVM, GCC
  * libbpf and dependencies

### Build & Run

1.  **Clone:**
    ```bash
    git clone https://github.com/YourUserName/LowLevelVpnMachine.git
    cd LowLevelVpnMachine
    ```
2.  **Build:**
    ```bash
    make
    ```
3.  **Run:**
    *Requires root privileges*
    ```bash
    sudo ./llvm_controller --iface <network_interface> --config <config_path>
    ```

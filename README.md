# 24-Hour Digital Clock using Flip-Flops

A digital electronics project implementing a **24-hour digital clock** using JK and D flip-flops, synchronous counters, divide-by-N counters, and combinational decoding logic.

## Overview

The project demonstrates the design of a sequential digital clock capable of counting:

* Seconds: `00–59`
* Minutes: `00–59`
* Hours: `00–23`

The clock is designed using flip-flop-based counters and combinational logic for state transitions, decoding, reset, and rollover conditions.

## Objectives

* Design a complete 24-hour digital clock using sequential logic.
* Understand and implement JK and D flip-flops.
* Design modular and divide-by-N counters.
* Implement rollover logic for seconds, minutes, and hours.
* Use combinational logic for decoding and control.
* Analyze timing and reset behavior in sequential circuits.

## Block Diagram

```text
                Clock Input
                     │
                     ▼
             ┌───────────────┐
             │ Seconds       │
             │ Counter       │
             │ 00 → 59       │
             └───────┬───────┘
                     │ Carry
                     ▼
             ┌───────────────┐
             │ Minutes       │
             │ Counter       │
             │ 00 → 59       │
             └───────┬───────┘
                     │ Carry
                     ▼
             ┌───────────────┐
             │ Hours         │
             │ Counter       │
             │ 00 → 23       │
             └───────┬───────┘
                     │
                     ▼
             ┌───────────────┐
             │ Display /     │
             │ Decode Logic  │
             └───────────────┘
```

## Key Components

### 1. Flip-Flops

JK and D flip-flops are used as the basic sequential storage elements.

They provide the state memory required for the counters and timing logic.

### 2. Divide-by-N Counters

The clock is divided into appropriate counting ranges:

```text
Seconds → 00–59
Minutes → 00–59
Hours   → 00–23
```

The counters generate carry signals when their respective limits are reached.

### 3. Rollover Logic

The rollover conditions are implemented using combinational logic.

For example:

```text
59 seconds → 00 seconds + carry to minutes
59 minutes → 00 minutes + carry to hours
23 hours   → 00 hours + rollover to 00
```

### 4. Reset Logic

Reset logic initializes the clock to a known state and ensures correct operation during rollover conditions.

## Design Flow

```text
Clock Input
     ↓
Frequency / Counter Logic
     ↓
Seconds Counter
     ↓
Minutes Counter
     ↓
Hours Counter
     ↓
Rollover & Reset Logic
     ↓
Display Decoding
```

## Technical Concepts

The project applies the following digital-design concepts:

* JK Flip-Flops
* D Flip-Flops
* Sequential Logic
* Synchronous Counters
* Divide-by-N Counters
* Combinational Logic
* State Transitions
* Reset Logic
* Rollover Detection
* Timing Analysis
* Digital Clock Design

## Challenges

During the design and debugging process, the main challenges included:

* Resolving timing mismatches between sequential blocks.
* Designing correct rollover conditions.
* Debugging reset behavior.
* Ensuring stable state transitions.
* Preventing incorrect transitions during counter rollover.

## Learning Outcomes

Through this project, I developed practical understanding of:

* Sequential digital circuit design.
* Flip-flop-based counter implementation.
* Clock division and frequency-based counting.
* Synchronous state transitions.
* Reset and rollover logic.
* Debugging timing-related issues in digital circuits.

## Project Structure

```text
EDC-LAB/
│
└── 24-hour clock/
    │
    ├── [Project files]
    └── README.md
```

## Applications

The concepts demonstrated in this project are applicable to:

* Digital clocks
* Timers
* Counters
* Frequency dividers
* Digital control systems
* Sequential logic systems
* FPGA/RTL-based digital designs

## Author

**Vinay Kurre**
B.Tech Electrical Engineering
IIT Hyderabad

GitHub: [VINAYKURREiith](https://github.com/VINAYKURREiith)

## Course

**Electronic Devices and Circuits (EDC) Lab**

Under the guidance of **Prof. Gajendranath Chowdary**

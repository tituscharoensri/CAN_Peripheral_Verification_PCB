# CAN_Peripheral_Verification_PCB

![PCB](./Images/PCB.jpg)

## Introduction

This is how to use my CAN Peripheral Verification PCB, and how to set up both nodes to test your CAN peripheral.

## Purpose
To easily Verify Transmission and Reception of CAN2.0A CANbus Peripheral for PCB bring up &amp; testing.
Previously to test CAN functionality in RedBack Racing, you would have to find a Nucleo board, CAN transceiver breakoutboard & Jumper wires... not to mention you would have to set up the nucleo board for reception or transmission. This adds an extra failure points during testing. The purpose of this PCB is so that you will only need to set up CAN on YOUR PCB, and configure the CAN reception & transmission ID's through DIP switches on this CAN Verification PCB in order to eliminate extra points of failure and wasted time due to finding components in lab and setting up 2 CAN peripherals.

## Features
- Tx ID (0b): Row representing 11 bit CAN packet Identifier to SEND.
- Rx ID (0b): Row representing 11 bit CAN packet Identifier that has been recieved.
- the 12th LED on the Tx ID (0b) row enables or disables continous attempts at CAN transmission. (Avoiding a "bus off" state when powered on without 2 nodes or improper hardware)
- Last Error Code (LEC): 3 bit error code that is referenced in the reference manual (STM32f446ret6).
- TxErr: Displays the occurance of a Transmission Error, more information can be found from the LEC.

### LED States:
- SOLID: 1/Enabled/Occurance
- Off: 0/Disabled/non-event


## Testing Process

### Setup and Preparation

Analog Signal Source: I set up a signal generator to produce a 1 kHz sine wave with an amplitude of 5V peak-to-peak, 2.5v DC offset.

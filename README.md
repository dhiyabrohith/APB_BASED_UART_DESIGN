# APB_UART
## Protocols Used
### [APB (Advanced Peripheral Bus)]

APB is part of ARM’s AMBA bus family and is used for connecting low-bandwidth peripherals like UART, GPIO, and timers.

### Key Features
Simple request–response protocol
Non-pipelined communication
Low power and low area design
Single transfer at a time

## Important APB Signals

| Signal   | Direction         | Description              |
|----------|------------------|--------------------------|
| PADDR    | Master → Slave   | Address bus              |
| PWRITE   | Master → Slave   | Read/Write control       |
| PSEL     | Master → Slave   | Peripheral select        |
| PENABLE  | Master → Slave   | Access phase indicator   |
| PWDATA   | Master → Slave   | Write data               |
| PRDATA   | Slave → Master   | Read data                |

## UART 16550
UART (Universal Asynchronous Receiver-Transmitter) is used for asynchronous serial communication.
### Features
- Configurable baud rate
- Full duplex communication
- Start and stop bit framing
- Error detection support
 ## UART Registers

| Register  | Function                          |
|-----------|-----------------------------------|
| THR       | Transmit Holding Register         |
| RBR       | Receiver Buffer Register          |
| IER       | Interrupt Enable Register         |
| IIR       | Interrupt Identification Register |
| FCR       | FIFO Control Register             |
| LCR       | Line Control Register             |
| LSR       | Line Status Register              |
| MCR       | Modem Control Register            |
| MSR       | Modem Status Register             |
| DIV1/DIV2 | Baud rate divisor registers       |
## Test Cases 
- Full Duplex Communication
- Half Duplex Communication
- Loopback Mode

## Conclusion

The APB-based UART 16550 core was successfully verified using the UVM methodology by validating UART communication, APB transactions, register functionality, interrupt generation, and various error conditions.

A comprehensive verification environment including driver, monitor, scoreboard, functional coverage, and RAL model was developed to ensure reliable verification of the DUT. Different test scenarios such as full duplex, half duplex and loopback mode conditions were thoroughly tested.

This project significantly enhanced understanding of:
- APB protocol and UART architecture
- UVM-based verification flow
- Register Abstraction Layer (RAL)
- Functional coverage concepts
- Debugging and problem-solving methodologies

Overall, the project provided strong practical exposure to industry-standard verification techniques and improved confidence in protocol-level verification and UVM environment development.

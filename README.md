# RAM-DESIGN


*COMPANY* : CODTECH IT SOLUTIONS

*NAME* : KULLAPPA CHAITANYA

*INTERN ID* : CT04DM114

*DOMAIN* : VLSI

*MENTOR* : NEELA SANTOSH

*DESCRIPTION OF THE TASK* :

The module, named sync_ram, has five ports: clk (clock), we (write enable), addr (address), din (data input), and dout (data output). The clk signal drives all synchronous operations. The we signal controls write operations; when it is high ('1'), the data on din is written into the memory at the specified address. The addr input specifies the address of the memory location to be accessed. The din input carries the data to be written into the RAM, while the dout output presents the data stored at the specified address.

The main functionality of the RAM is implemented inside a synchronous process that is sensitive to the rising edge of the clock. During each rising clock edge, the process checks if the we (write enable) signal is high. If so, the data from the din input is written into the RAM at the address specified by addr. Regardless of whether a write occurs, the data stored at the address is read and assigned to an internal signal dout_reg, which is then assigned to the output dout outside the process. This ensures that the output data is registered and available for use in synchronous logic.

This design ensures predictable timing behavior suitable for use in clocked digital systems such as FPGAs or ASICs. The RAM operates synchronously, meaning both read and write operations are controlled by the clock signal, which simplifies timing analysis and integration into larger designs. The design also follows good VHDL practices such as using unsigned for address conversion and employing generics for reusability.

The current behavior provides old data during a simultaneous read and write to the same address, which is typical for many RAM blocks. If desired, this behavior can be changed to output the new data by modifying the process logic, although this depends on the synthesis tool and target hardware capabilities.

Overall, the code presents a robust, parameterizable synchronous RAM module suitable for a wide range of digital design applications. It demonstrates clean architecture, efficient use of VHDL constructs, and adherence to design principles needed for synthesizable hardware description. This module could be easily extended or integrated into more complex systems such as processors, buffers, or digital signal processing architectures.

OUTPUT :

<img width="754" alt="Image" src="https://github.com/user-attachments/assets/726ec24e-10b1-4eb5-9193-9d2bcd2b67e1" />

<img width="784" alt="Image" src="https://github.com/user-attachments/assets/45b7c80d-7aac-47e2-a1d2-057bb7e8da1b" />

<img width="785" alt="Image" src="https://github.com/user-attachments/assets/f47d28af-b68a-4a80-8300-4be1329a0cb0" />

<img width="786" alt="Image" src="https://github.com/user-attachments/assets/28542457-17cf-4217-a4dc-f535d854c61e" />







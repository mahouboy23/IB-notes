---
tags: EE
---

# Extended essay

 **Subject:** Computer science
 
 **TOPIC:** Comparaison des architectures de mémoire à accès aléatoire et de leur effet sur la performance
 
 >[!Research question:]
 > Dans quelle mesure le NVDIMM affecte-t-il les performances par rapport au VDIMM dans un système ?
 
 
A **NVDIMM** (pronounced "en-vee-dimm") or **non-volatile DIMM** is a type of persistent [random-access memory](https://en.wikipedia.org/wiki/Random-access_memory "Random-access memory") for computers using widely used [DIMM](https://en.wikipedia.org/wiki/DIMM "DIMM") form-factors. [Non-volatile memory](https://en.wikipedia.org/wiki/Non-volatile_memory "Non-volatile memory") is memory that retains its contents even when electrical power is removed, for example from an unexpected power loss, system crash, or normal shutdown. Properly used, NVDIMMs can improve application performance and system crash recovery time. They enhance [solid-state drive](https://en.wikipedia.org/wiki/Solid-state_drive "Solid-state drive") (SSD) endurance and reliability.

Many "non-volatile" products use volatile memory during normal operation and dump the contents into non-volatile memory if the power fails, using an on-board backup power source. Volatile memory is faster than non-volatile; it is byte-addressable; and it can be written to arbitrarily, without concerns about wear and device lifespan. However, including a second memory to achieve non-volatility (and the on-board backup power source) increases the product cost compared to volatile memory.

There are many emerging non-volatile memories in development and a few that have been launched including [Magnetoresistive RAM](https://en.wikipedia.org/wiki/Magnetoresistive_RAM "Magnetoresistive RAM") (MRAM) and Intel's [3D XPoint](https://en.wikipedia.org/wiki/3D_XPoint "3D XPoint"). Like MRAM, [Nano-RAM](https://en.wikipedia.org/wiki/Nano-RAM "Nano-RAM") based on [carbon nanotubes](https://en.wikipedia.org/wiki/Carbon_nanotube "Carbon nanotube") is one technology intended to come close to DRAM on the criteria of performance, byte-addressability and device lifespan; first products are expected in 2021 at moderate density, from fabrication partner Fujitsu. The goal of this technology is able to scale cost-effectively scale out so persistent memory could replace DRAM as the main system memory in enterprise systems.


**What is it?** 
DIMM stands for dual in-line memory module; more commonly, it is called a RAM stick. It is a long, thin strip of printed circuit board containing RAM (random access memory) chips, with pins that connect it directly to a motherboard.  
  
DIMM has become the predominant type of memory modules on the market because it is natively 64 bits, allowing for faster data transfer than its 32-bit SIMM (single in-line memory module) predecessor, while consuming less power. Common types of DIMMs include UDIMMs (unbuffered DIMMs), FB-DIMMs (fully-buffered DIMMs), RDIMMs (registered DIMMs).
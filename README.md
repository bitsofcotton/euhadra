# euhadra
(planning stub) bear metal virtual machine executer.

# Description
Execute NAND described simple_pmpu virtualmachine on some specific bearmetal computer.
We need one binaried virtual base program.

# Later
We need to implement simple_pmpu and NAND first, so this has no chance at least in a year.

# Recursive on system
We should implement recursive on this with very slow but at least guarantee integrity in some range.
But if so, if the computer is intruded as remote memory dump/write,
we need to replace whole kernel image randomly real/virtual and recompile as
hard to read ones before the intruder analyze because the intruder can do so
memory addresses to inject codes.
This method is redusable into recompile/reload the kernel in some interval.
To guarantee in some range, we need to do them in 2nd order virtual, 1st order not to track memory addresses by low layers, 2nd order to separate each systems by low layers with some whole system cryption. So cryption itself is to make hard to read ones when the data is enough, the system should be separated in such system.

# Detection
If some process nor datas modified into userland, mostly kernel has the
data on them. If we dump kernel space / process info / disk info and so on,
we can detect them in such case.
Otherwise, it's an malicious codes parallel to the kernel, in such case,
if there's a differ on each CPU tick and RTC, it has a chance to be intruded.
Otherwise, the differ of tick time out of the box has a difference to
the machine, it also should because xtal is stable to some of the environments.
(In fact, we need to calculate sup of the tick uncertainity \% on whole box in
ideal hardware with real environment meaning.)  
XXX: but if the malicious process have its core which is hidden from kernel land
and running all the time with some trigger, only the some race condition they occur
in rare case can detect them.

# Process separation
Also, if we run binaries on VMs, we need to separate some execution binaries intend to break continuity on execution space meaning. Breaking continuity on meaning causes harder to attack the surface (but it is still able to infect in principle).

# This is concept and only a compileable document.
We must search preceding patents first before to compile or use.


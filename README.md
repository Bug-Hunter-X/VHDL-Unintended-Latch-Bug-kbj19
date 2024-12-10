# VHDL Unintended Latch Bug

This repository demonstrates a common VHDL coding error that results in an unintended latch.  The bug occurs because a signal (`data_reg` in this example) is assigned a value conditionally within a process, but there is no assignment in the `else` condition.  This causes the simulator to infer a latch to maintain the previous value of the signal when the conditional assignment is not executed. 

The solution shows how to avoid this by ensuring a value is assigned to the signal in all branches of the process.
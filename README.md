Adding a `breakpoint()` in the code will set a breakpoint at that line, and the program will enter `pdb` when it reaches that point.

### Commands to inspect the current state in `pdb`:
- `p` -- (print) Prints a variable, can print any valid Python expression.
- `w` -- (where) Shows the call stack.
- `l` -- (list) Displays the source code around the current line, by default 11 lines.
- `l.` -- Returns to the current line.
- `ll` -- (long list) Shows all the code in the current function.
- `u` -- (up) Moves up one frame in the call stack.
- `d` -- (down) Moves down one frame in the call stack.

### Commands to control the program in `pdb`:
- `n` -- (next) Executes the current line.
- `s` -- (step) Steps into a function if the current line contains a function call.
- `retval` -- Retrieves the return value of the function.
- `until` -- Runs until a line number greater than the current line is reached, useful for exiting loops during debugging.
- `until 10` -- Runs until reaching line number 10 or greater.
- `r` -- (return) Stops at the return point of the current function.
- `lst = [1,2,3]` -- You can manually modify any variable in `pdb`.
- `c` -- (continue) Continues execution until the next breakpoint.

### How to debug without modifying the code:
- `python -m pdb example.py` -- Enters `pdb` mode directly without adding breakpoints in the code.

### Managing breakpoints:
- `b` -- (break) Lists all breakpoints.
- `b 5` -- (break) Sets a breakpoint at line 5 from the command line in `pdb` mode. You can use `ll` to view the code and `c` to continue until the breakpoint.
- `q` -- (quit) Exits the debugger.
- `b inspect.currentframe` -- (break) Sets a breakpoint in a third-party library function in `pdb` mode.
- `clear` -- Clears all breakpoints.
- `clear 1` -- Clears the first breakpoint.

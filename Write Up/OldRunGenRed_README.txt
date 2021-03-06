To run the Generator and Reducer:
    1. Run RunGenRed.py
    2. Copy circuitCNF.txt to input.cnf for SAT Solver
    3. Run SAT Solver on input.cnf

The Generator takes in parameters numIn, numGates, fanin, and depth. It 
generates a list of Gate objects, and writes this list to the file circuit.txt.
Each line of circuit.txt is a Gate object.

The Reducer takes in the circuit generated by the Generator as its only parameter.
The circuit is passed directly from the Generator to the Reducer in RunGenRed.py
to reduce errors that could come from having the reducer read the circuit.txt file.

RunGenRed.py allows us to set parameters for the generator, as well as run both the
Generator and Reducer with one script. When it runs, it will make a circuit.txt file
(from the Generator) and a circuitCNF.txt file (from the Reducer). Use the 
circuitCNF.txt file with your desired SAT Solver. When RunGenRed.py runs successfully,
it will print the number of inputs for the circuit to the console. This is helpful
when reading the output.cnf of the SAT Solver, as we only care about the assignments
for the input gates.

The parameters for the Generator and Reducer are somewhat restricted currently.
There is a lot of room to experiment with variable parameters.
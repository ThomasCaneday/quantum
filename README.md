# Quantum Circuit Preparation: `quantum_circuit.py`

This program demonstrates how to construct, execute, and measure a quantum circuit using **Qiskit**, a Python library for quantum computing. The circuit prepares a quantum state \(|000\rangle + i|111\rangle\), applies a series of quantum gates, measures the qubits, and retrieves a quasi-probability distribution from the measurement results.

---

## Features
1. **Quantum State Preparation:**
   - Creates a 3-qubit quantum circuit.
   - Constructs the state \(|000\rangle + i|111\rangle\) using a combination of quantum gates.

2. **Classical Measurement:**
   - Adds classical measurements to all qubits.

3. **Execution:**
   - Executes the circuit using the Qiskit **Sampler** primitive with 1000 shots.
   - Outputs the quasi-probability distribution from the measurement.

---

## Requirements
- Python 3.8 or later
- [Qiskit](https://qiskit.org/) library

Install Qiskit using pip if you don't already have it:

```bash
pip install qiskit
```

---

## Code Overview

1. **Quantum Circuit Construction**  
   Prepares the desired quantum state:
   - Hadamard gate (`H`) on qubit 0 to create superposition.
   - Phase gate (`P`) to add a relative phase to \(|000\rangle\).
   - Controlled-NOT gates (`CX`) to entangle qubit 0 with qubits 1 and 2.

2. **Measurement:**  
   Adds measurement to all qubits without modifying the original circuit.

3. **Execution:**  
   The circuit is executed using the **Sampler** primitive, and the result is displayed as a quasi-probability distribution.

---

## Usage

1. Save the script as `quantum_circuit.py`.
2. Run the program in your terminal or Python environment:

```bash
python quantum_circuit.py
```

3. The output will display a quasi-probability distribution representing the measurement results of the quantum circuit.

---

## Output Example

```text
> Quasi probability distribution: {state_1: value_1, state_2: value_2, ...}
```

The keys (`state_1`, `state_2`, etc.) represent the measured states in binary format, and the values represent their quasi-probability.

---

## Notes
- This example uses the **Sampler** primitive, a feature introduced in recent versions of Qiskit for efficient sampling and simulation.
- If executed on a quantum device, noise may affect the results.
